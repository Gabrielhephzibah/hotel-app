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

					
				</div>
				
			</div>
			
		</div> <!-- clossing tag for first row
		 -->
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
		border: 1px solid #fff;
		height: 551px;
		background-color: #131313;

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

	

</style>