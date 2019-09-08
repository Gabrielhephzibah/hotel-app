<template>
	<div class="wrapper">
		<div class="row" style="max-width:1330px;">
			<div class="col-12">
				<div class="firstRow" style="max-width:1330px;">
					<img  class="img1" src="../assets/copy3.png" alt="ggg">
					<img class="img2" src="../assets/name.png" alt="huu">
					<div class="login">
						<router-link :to="{name:'login'}">
						<img class="img3" src="../assets/login.png" alt="hhhh">
					</router-link>
						
					</div>
					
					
				</div>
				
			</div>
			
		</div>
		<hr>

		<div class="row" style="max-width:1330px;margin-top: -15px;">
			<div class="col-4" style="padding-right: 0px; padding-left: 0px;">
				<div class="left">
					<div>
						<h1 class="room pt-1">Accomodation</h1>
						<p class="offer pt-4">We offer a variety of boutique accomodation that combines comfort, style, elegance and the latest technology</p>
						
					</div>
					
				</div>

				
			</div>

			<div class="col-8"style="padding-right:0px; padding-left:5px;">
				<div class="right">
					<img  class="img4" src="../assets/room7.png" height="100%">
					
				</div>
				
			</div>
			
		</div>
		<hr>

		<div class="row"style=" max-width:1330px; padding-right:0px;margin-top: -15px;">
			<div class="col-8"style="padding-right: 0px; padding-left: 0px;">
				<div class="left2">
					<img style="margin-left:-113px;" class="img5" src="../assets/rest2.png" height="100%">
				</div>

				
			</div>

			<div class="col-4"style="padding-right:0px; padding-left:5px;">
				<div class="right2">
					<h1 class="room pt-4">Restaurant</h1>
						<p class="offer pt-4">Our 5 star restaurant offers tantalizing African and intercontinental inspired cuisine in an authentic atmosphere</p>


				</div>
				
			</div>
		</div>


		
	</div>

</template>








<!-- <template> -->

	<!-- <div class="wrapper" style="max-width:1200px;">
		<div class="row"style="max-width:1200px;" >
			<div class="col-12">
				<div class="firstRow">
					<img style=" width:100%; height:100%;" class="img1" src="../assets/firstimg3.png" alt="hmm">
					<img class="img2" src="../assets/name.png" alt="huu">
					<div class="login">
						<router-link :to="{name:'login'}">
						<img class="img3" src="../assets/login.png" alt="hhhh">
					</router-link>
						
					</div>
					
					
				</div>

				
			</div> -->
			
		<!-- </div> --><!-- closing div for first row -->
		<!-- <hr>

		<div class="row" style="max-width:1200px;margin-top: -15px;">
			<div class="col-4" style="padding-right: 0px; padding-left: 0px;">
				<div class="left">
					<div>
						<h1 class="room pt-4">Accomodation</h1>
						<p class="offer pt-4">We offer a variety of boutique accomodation that combines comfort, style, elegance and the latest technology</p>
						
					</div>
					
				</div>

				
			</div>
			<div class="col-8" style="padding-right:0px; padding-left:5px;">
				<div class="right">
					<img style="width:100%" class="img4" src="../assets/room2.png" height="100%">
					
				</div>
				
			</div>

			 -->
		<!-- </div> --> <!-- closing div for the second div -->
		<!-- <hr>
		<div class="row" style="max-width:1400px;margin-top: -15px;">
			<div class="col-8" style="padding-right: 0px; padding-left: 0px;">
				<div class="left2">
					<img style="margin-left:-113px;" class="img5" src="../assets/rest2.png" height="100%"> -->
					<!-- <div>
						<h1 class="room mt-4">Accomodation</h1>
						<p class="offer">We offer a variety of boutique accomodation that combines comfort, style, elegance and the latest technology</p>
						
					</div> -->
				<!-- 	
				</div>


				
			</div>
			<div class="col-4" style="padding-right:0px; padding-left:5px;">
				<div class="right2">
					<!<img class="img4" src="../assets/.png" height="100%"> -->
					 <!-- <div>
						<h1 class="room pt-4">Restaurant</h1>
						<p class="offer pt-4">Our 5 star restaurant offers tantalizing African and intercontinental inspired cuisine in an authentic atmosphere</p>
						
					</div> 

					
				</div>
				
			</div>
 --> 
			
		<!-- </div> --> <!-- closing div for the third div -->




		
	<!-- </div> closing div for wrapper - -->

	
<!-- </template> -->


<style scoped>

hr{ 
	height:2px;
	background-color: #fff;
	margin-top: 1px;

 }
.wrapper{
	height:142vh;
	/*border:1px solid red;*/
	/*overflow-x: hidden;*/
}

.firstRow{
	height:306px;
	/*border:1px solid blue;*/
	width: 221.5vh;
}

.img1{

	position:absolute;
	/*margin-left:-19px;*/
	z-index: -1;
	left: 0px;
  	top: 0px;
  	/*max-width: 13350px;*/

}

.img4{
	left: 0px;
  	top: 0px;
}

.img5{
	left: 0px;
	top: 0px;
}

.img2{
	float: left;
    /*mag/in-left: 105px;*/
    margin-left: 205px;
    margin-top: 68px;
}

.img3{
	float: left;
    margin-left: -532px;
    padding-top: 218px;

}

.left{
	border:0px solid #fff;
	height: 302px;
	background-color: #98A2A4;
	margin-left: 13px;

}

.left2{
	border:0px solid #fff;
	height: 310px;

	margin-left: 13px;
}

.right{
	border:0px solid #fff;
	height: 302px;
	/*background-color:*/ 
}

.right2{
	border:0px solid #fff;
	height: 310px;
	background-color: #90AA8F;
	width: 456px;
    margin-left: 13px;



}

.room{
font-family: Eczar;
font-style: normal;
font-weight: 600;
font-size: 30px;
line-height: 53px;

color: #000000;

}

.offer{
font-family: Lato;
font-style: normal;
font-weight: 600;
font-size: 22px;
line-height: 44px;
text-align: center;

color: #000000;
width: 100%;
}
	



</style>