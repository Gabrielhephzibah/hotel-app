<template>
	<div class="wrapper">
		<div class="row"style="max-width:1200px;">
			<div class="col-12">
				<div class="inside d-flex justify-content-center">
					<div class="box">
						<form  @submit.prevent="login">
						  <div class="form-group">
						    <label class="text1">Name</label>
						    
						    <input type="name" v-model="guest.name" class="form-control mt-3" id="name" aria-describedby="name" placeholder="Enter your name">
				
						  </div>
						  <div class="form-group pt-4">
						    <label class="text1">Password</label>
						    <input type="password" v-model="guest.password" class="form-control mt-3" placeholder=" Enter your Password">
						  </div>
						  <div class="pt-5">
						  	<!-- <router-link :to="{name:'dashboard'}"> -->
						  	<button type="submit" class=" log btn btn-light"><small class="small">LOG IN</small></button>
						  <!-- </router-link> -->
						  	
						  </div>
						  
						</form>
						
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
        guest:{
        	name: "",
        	password: ""
        },
        error:{}

      }
    },

    components:{},
    mounted() {},

  methods:{
  	login:function() {
  		this.$http.post('http://localhost:5000/user/login',{
  			name:this.guest.name,
  			password:this.guest.password
  		})
      .then(response =>{
        console.log(response)
        // this.guest = response.data
        console.log(this.guest)
        this.$router.push("/dashboard")
      })
    }

  	}
  };

  
  
  </script>


<style scoped>

	form{
		padding-top: 41px;
	}
	
	input {
		width: 250px;
		margin: auto;

	}
	.wrapper{
		height: 100vh;
		background-color: #98A2A4; 
	}

	.inside{
		/*border:1px solid black;*/
		height: 100vh;
	}

	.box{
		/*border:1px solid #fff;*/
		width: 340px;
		height: 432px;
		/*background-color: blue;*/
		margin-top: 145px;
		background: #EEF1F6;
		border-radius: 41px;
		margin-left: 200px;
	}

	.text1{
		font-family: Lato;
		font-style: normal;
		font-weight: bold;
		font-size: 23px;
		line-height: 29px;
		/* identical to box height */


		color: #1D1F34;

	}

	.log{
		width: 121px;
		height: 40px;
		background-color: #fff;
	}

	.small{
		font-family: Lato;
		font-style: normal;
		font-weight: bold;
		font-size: 20px;
		line-height: 29px;
		/* identical to box height */


		color: #1D1F34;

	}
	
	.log:hover{
		background-color: #007bff;
		color: #000;
	}



</style>