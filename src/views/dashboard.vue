<template>
	<div class="wrapper">
		<div class="row" style="max-width:1513px;">
			<div class="col-8">
				<div class="leftImg">
					<img class="img1" src="../assets/night2.png" alt="you">
					<img class="img2"  src="../assets/enjoy.png" alt="enjoy">
					
				</div>
				
			</div>
			<div class="col-4" style="padding-right:0px;">
				<div class="rightText">
					<img src="../assets/hotel.png" alt="hotel">
					<p class="multi">Multi award boutique hotel nestled on 10 acres in the very heart of Hunter's Valley wine country</p>

					
				</div>
				
			</div>
			
		</div> <!-- clossing tag for first row-->


		<div class="second">
			<div class="row "style="max-width:1513px;">
				<div class="col-6">
					<div class="first d-flex justify-content-left">
						<router-link :to="{name:'checkin'}">
						<img src="../assets/check.png" alt="check">
					</router-link>
						
					</div>
					
				</div>
				<div class="col-6">
					<div class="side">
						<router-link :to="{name:'guest'}">

						<img src="../assets/guest.png"><span class="guest pt-4">Guest</span>
					</router-link>
						
					</div>
					
				</div>

				
			</div>

			
		</div>
		
	</div> <!-- closing tag for wrapper -->
	
</template>



<style scoped>
	.wrapper{
		border:1px solid black;
		height: 200vh;
		/*background-color: #131313;*/
	}

	.leftImg{
		/*border: 1px solid #fff;*/
		height:551px; 
	}

	.rightText{
		/*border: 1px solid #fff;*/
		height: 551px;
		background-color: #131313;
		padding-top: 79px;

	}

	.img1{

	position:absolute;
	/*margin-left:-19px;*/
	z-index: -1;
	left: 0px;
  	top: 0px;

	}

	.img2{
		margin-top: 200px;
	}

.multi{
	font-family: Lato;
	font-style: normal;
	font-weight: bold;
	font-size: 33px;
	line-height: 54px;

	color: #FDFCFA;
	margin-top: 35px;
	text-align: left;
	margin-left: 73px;

}

.second{
	background-color: #131313;
	height: 50vh;
}

.first{
	/*border:1px solid #fff;*/
	height: 15vh;
	margin-top:120px;
	margin-left: 33px;
}

.side{
	/*border:1px solid #fff;*/
	height: 15vh;
	margin-top: 100px;
	float:right;
	margin-right: 70px;

}
.guest{
	font-family: Lato;
	font-style: normal;
	font-weight: bold;
	font-size: 43px;
	line-height: 52px;
	/* identical to box height */


	color: #FDFCFA;

}
	

</style>