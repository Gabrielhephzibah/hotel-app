<template>
	<div class="wrapper">
		<div class="row" style="max-width:1200px;">
			<div class="col-7">
				<div class="left">
						<div class="great">
							<router-link :to="{name:'dashboard'}">
							<img src="../assets/great3.png">
						</router-link>
							
						</div>
					<div class="info pt">
						<h3 class="fill">Please fill in your information</h3>
						
					</div>
					<form class="form1" @submit.prevent="add">
					  <div class="form-row">
					    <div class="col-6">
					    <label class="name">First name</label>
					      <input type="text" v-model="guest.first_name"  class="form-control mt-5" placeholder="First name">
					    </div>
					    <div class="col-6">
					    <label class="name">Last name</label>
					      <input type="text" v-model="guest.last_name" class="form-control mt-5" placeholder="Last name">
					    </div>
					  </div>

					  <div class="form-row pt-5">

					  	 <div class="form-group col-6">
					          <label class="name">Sex &nbsp; &nbsp; &nbsp;&nbsp;</label>
					          <select id="inputState" v-model="guest.sex" class="form-control mt-5">
					            <option selected>Choose...</option>
					            <option>Male</option>
					            <option>Female</option>
					          </select>
					        </div>
					        <div class="col-6">
					        <label class="name">Room number</label>
					          <input type="text" v-model="guest.room_number" class="form-control mt-5" placeholder="Room number">
					        </div>
					  
					  </div>

					  <!-- <div class="form-row pt-5">
					    <div class="col-6">
					    <label class="name">Room number</label>
					      <input type="text" class="form-control mt-5" placeholder="First name">
					    </div> -->

					    <div class="form-row pt-5">
					    <div class="form-group col-6">
					          <label class="name">Room type</label>
					          <select id="inputState" v-model="guest.room_type" class="form-control mt-5">
					            <option selected>Choose...</option>
					            <option>Single</option>
					            <option>Double</option>
					            <option>Triple</option>
					             <option>Queen</option>
					              <option>King</option>
					              <option>Twin</option>
					              <option>Double-Double</option>
					          </select>
					        </div>

					        <div class="form-group col-6">
					          <label class="name">Purpose for Stay</label>
					          <select id="inputState" v-model="guest.purpose_for_stay" class="form-control mt-5">
					            <option selected>Choose...</option>
					            <option>Buisiness</option>
					            <option>Vacation</option>
					            <option>Others</option>
					          </select>
					        </div>
					   
					  </div>

					 <!--  <div class="form-row pt-5">
					    


					     <div class="form-group col">
					          <label class="name">Purpose for Stay</label>
					          <select id="inputState" class="form-control mt-5">
					            <option selected>Choose...</option>
					            <option>Buisiness</option>
					            <option>Occasion</option>
					            <option>Tour</option>
					          </select>
					        </div> -->



					    <!-- <div class="col">
					    <label class="name">Purpose for Stay</label>
					      <input type="text" class="form-control mt-5" placeholder="Last name">
					    </div> -->
					  <!-- </div> -->

					  	<div class="pt-5">
						  	<!-- <router-link :to="{name:'dashboard'}"> -->
						  	<button type="submit" class=" log btn btn-light"><small class="small">ADD TO GUESTS</small></button>
						  <!-- </router-link> -->
						  	
						  </div>

					</form>

					
				</div>
				
			</div>

			<div class="col-5">
				<div class="right">
					<img src="../assets/stay3.png" alt="stay">

					<div class="correct">
						<img src="../assets/correct.png"><span class="best">Best Stay Guaranteed</span>
						
					</div>
					
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
        guest: {
        	first_name:"",
        	last_name:"",
        	sex:"",
        	room_number:"",
        	room_type:"",
        	purpose_for_stay:""
        },
        error:{}

      }
    },

    components:{},
    mounted() {},
     methods:{
      add:function(){
  		console.log(this.guest)
       	 this.$http.post('http://localhost:5000/hotel/add',this.guest)
      	.then(response=>{
	      console.log(response)
	      this.guest= response.data
	      console.log(this.guest)

    	})
  
      }
    }
  };

  
  
  </script>






<style scoped>
	label{
		display: block;
	}



	.wrapper{
		/*border: 1px solid black;*/
		height: 113vh;
	}

	.left{
		/*border: 1px solid blue;*/
		height: 113vh;
		background-color: #EEF1F6;
		padding-top: 
	}

	.right{
		/*border: 1px solid red;*/
		height: 98vh;


	}

	input {
		width: 300px;
		margin-left: 20px;
		height: 55px;


	}

	select{
		width: 300px;
		margin-left: 20px;
		height: 55px;

	}

	.fill{
		padding-top: 44px;
		font-family: Lato;
		font-style: normal;
		font-weight: bold;
		font-size: 30px;
		line-height: 36px;
		/* identical to box height */


		color: #000000;

	}

	.form1{
		padding-top: 34px;
	}

	.name {
		float: left;
		margin-left: 20px;
		font-family: Lato;
		font-style: normal;
		font-weight: bold;
		font-size: 27px;
		line-height: 36px;
		 /*identical to box height */


		color: #000000;


	}

	.log{
		width: 189px;
		height: 40px;
		background-color: #fff;
		float: left;
		margin-left: 30px;
		 border-color: #4CAF50;
		 border: 1px solid #007bff;
	}

	.log:hover {
		background-color: #007bff;
		color: #000000;

	}

	/*.success {
  border-color: #4CAF50;
  color: green;
}

.success:hover {
  background-color: #4CAF50;
  color: white;
}*/

	.small{
		font-family: Lato;
		font-style: normal;
		font-weight: bold;
		font-size: 17px;
		line-height: 24px;

		color: #000000;

	}

	.best{
		margin-left: 20px;
		font-family: Lato;
		font-style: normal;
		font-weight: normal;
		font-size: 28px;
		line-height: 34px;
		/* identical to box height */


		color: #1D1F34;

	}

	.correct{
		margin-top: 20px;

	}
	.great{
		float: left;
		margin-top: 20px;
		    margin-left:8px;
	}

	
</style>