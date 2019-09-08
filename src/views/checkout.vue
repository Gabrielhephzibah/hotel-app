<template>
	<div class="wrapper">
		<div class="row" style="max-width:1200px;">
			<div class="col-8">
				<div class="left">
					<div  class="head" >
						<h5 class="slip">Guest Check-out Slip</h5>
						
					</div>

					<div v-if="guest" class="inside">
						<hr>
						<div class="first">
							<h5 class="clay">First name <span>{{guest.first_name}}</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Last name <span>{{guest.last_name}}</span></h5>
							
						</div>
						<hr>

						<div class="first">
							<h5 class="clay">Sex <span>{{guest.sex}}</span></h5>
							
						</div>
						<hr>

						<div class="first">
							<h5 class="clay">Room number</rp> <span>{{guest.room_number}}</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Room type<span>{{guest.room_type}}</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Purpose for stay<span>{{guest.purpose_for_stay}}</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Check-in-time <span>{{guest.check_in_time | fineDate}}</span></h5>
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Check-Out-time <span>{{guest.check_out_time | fineDate}}</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="final clay">Final Bill <span>${{guest.final_bill}}</span></h5>
							
						</div>
						<hr>
					</div>
					
				</div>
				
			</div>

			<div class="col-4">
				<div class="right">
					<img class="arrow" src="../assets/arrow.png" @click="PrintWindow">
					
				</div>
				
			</div>
			
		</div>
		
	</div>
	
</template>
	
	<script>
  export default{
    name:'home',
    props: ['id'],
    data() {
      return{
        apiResponse:{},
        guest: {},
        error:{}

      }
    },

    methods:{
    	PrintWindow: function() {
    		this.$nextTick(() => {
    		    window.print();
    		  });
    	}
    },

    components:{},
    mounted() {
      let id = this.$route.params.id
      // console.log(this)
      this.$http.get('http://localhost:5000/hotel/single/'+id)

      .then(response =>{
        console.log(response)
        this.guest = response.data
      //   console.log(this.guest)
      })
    },

  	filters: {
  		fineDate: function (val) {
  			return new Date(val).toGMTString()
  		}
  	}

  };



  
  
  </script>



<style scoped>

	hr{
		height: 1px;
		background-color:  #000000;
		width: 100%;

	}

	span{
		float: right;
		/*vertical-align: right;*/
		margin-right: 67px;
	}

	.wrapper{
		/*border: 1px solid green;*/
		height: 120vh;
		background-color:#EEF1F6;
	}

	.left{
		height: 94vh;
		/*border: 1px solid red;*/
		margin-left: 23px;

	}

	.right{
		height: 94vh;
		/*border: 1px solid orange;*/
	}

	.inside{
		height: 100vh;
		/*border: 1px solid black;*/
		/*width: 123vh;*/
		margin: auto;
		padding-top: 41px;
		background-color: #FDFCFA;
	}

	.table1{
		background-color: #FDFCFA;
	}

	.slip{
		padding-top: 15px;
		font-family: Lato;
		font-style: normal;
		font-weight: 300;
		font-size: 33px;
		line-height: 40px;
		/* identical to box height */


		color: #000000;

	}

	.clay{
		text-align: left;
		margin-left: 70px;
		font-family: Lato;
		font-style: normal;
		font-weight: 550;
		font-size: 22px;
		line-height: 29px;
		/* identical to box height */


		color: #000000;

	}

	.first{
		height: 30px;
		/*border: 1px solid red;*/
	}

	.final{
		font-family: Lato;
		font-style: normal;
		font-weight: 800;
		font-size: 24px;
		line-height: 29px;
		/* identical to box height */


		color: #000000;

	}

	.arrow{
		padding-top: 322px;
		margin-left: 320px;
	}

	
</style>