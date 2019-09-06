<template>
	<div class="wrapper">
		<div class="guest">
			<h5 class="text">GUEST LIST</h5>
			<div class="row"style="max-width:1513px;" >
				<div class="col-12">
					<table class=" table1 table table-dark">
					  <thead>
					    <tr>
					      <th scope="col" style="vertical-align:middle;">#</th>
					      <th scope="col" style="vertical-align:middle;">First name</th>
					      <th scope="col" style="vertical-align:middle;">Last name</th>
					      <th style="vertical-align:middle;" scope="col"></th>
					    </tr>
					  </thead>
					  <tbody>
					    <tr v-for="(guest,hephzibah) in guests">
					      <th scope="row">{{ hephzibah + 1 }}</th>
					      <td class="robert"style="vertical-align:middle;">{{ guest.first_name }}</td>
					       <td class="robert"style="vertical-align:middle;">{{guest.last_name}}</td>
					      <td>
					      	<div class="img">
					      		<!-- <router-link :to="{name:'checkout', params:{id:guest._id}}"> -->
					      		<a @click.prevent="checkOut(guest)" href="#">
					      			<img src="../assets/checkarrow2.png" alt="checkinihh">
					      		</a>
					      		<!-- </router-link> -->
					      		
					      	</div>
					      </td>
					      <!-- <td>@mdo</td> -->
					    </tr>
					   </tbody>
					</table>
					
				</div>
				
			</div>
			
		</div>
		
	</div>
	
</template>


<script>
export default{
  name:'home',
  data() {
    return{
      apiResponse:{},
      guests:[],
      error:{},
      formdata: {}
    };
  },
  mounted() {
    this.$http.get('http://localhost:5000/hotel')
    .then(response =>{
      // console.log(response)
      this.guests = response.data
      console.log(this.guest)
    })
  },
  methods:{
  	checkOut: function(guest){
  		let amountPerMin = 10;
  		let checkInTime = new Date(guest.check_in_time)
  		let checkOutTime = new Date();

  		let totalMinsSpentInMilisecs = checkOutTime - checkInTime

  		let totalMinsSpentInMins = Math.round(((totalMinsSpentInMilisecs % 86400000) % 3600000) / 60000); // minutes

  		let finalBill = amountPerMin * totalMinsSpentInMins

  		this.formdata.check_out_time = checkOutTime
  		this.formdata.final_bill = finalBill
  		this.formdata.has_checked_out = true

  		this.$http.put('http://localhost:5000/hotel/update/'+guest._id, this.formdata)
  			.then(response=>{
  				this.$router.push({name: 'checkout', params: {id: guest._id} })
  			})
  			.catch(error=>{
  				console.log(error)
  			})
  	}
  }
};



</script>



<style scoped>
	.wrapper{
		/*border:1px solid red;*/
		height: 200vh;
		background-color: #232121;
	}

	.text{
		margin-top: 0px;
		font-family: Eczar;
		font-style: normal;
		font-weight: bold;
		font-size: 36px;
		line-height: 64px;

		color: #FDFCFA;

	}

	tr{
		height: 90px;
		vertical-align: middle;
	}

	th{
		margin-bottom: 30px;
		vertical-align: middle;
		font-family: Eczar;
		font-style: normal;
		font-weight: bold;
		font-size: 30px;
		line-height: 89px;
		/* identical to box height */


		color: #FDFCFA;

	}

	.table1{
		background-color:  #232121;
	}

	/*table td, .table1 th {
    padding: .75rem;
    vertical-align: top;
    border-top: 1px solid #fff;
}
	*/

	.robert{
		font-family: Lato;
		font-style: normal;
		font-weight: bold;
		font-size: 30px;
		line-height: 60px;
		/* identical to box height */


		color: #FDFCFA;

	}

	.img{
		float: right;
	}

</style> 
	

