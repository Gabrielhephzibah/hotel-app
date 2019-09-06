<template>
	<div class="wrapper">
		<div class="row" style="max-width:1513px;">
			<div class="col-8">
				<div class="left">
					<div class="head">
						<h5 class="slip">Guest Check-out Slip</h5>
						
					</div>

					<div class="inside">
						<hr>
						<div class="first">
							<h5 class="clay">First name <span>Claire</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Last name <span>Robert</span></h5>
							
						</div>
						<hr>

						<div class="first">
							<h5 class="clay">Sex <span>Female</span></h5>
							
						</div>
						<hr>

						<div class="first">
							<h5 class="clay">Room number</rp> <span>RM 33</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Room type<span>Royalty</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Purpose for stay<span>Buisiness</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Check-in-time <span>8:00pm</span></h5>
						</div>
						<hr>
						<div class="first">
							<h5 class="clay">Check-Out-time <span>9:00pm</span></h5>
							
						</div>
						<hr>
						<div class="first">
							<h5 class="final clay">Final Bill <span>$3000</span></h5>
							
						</div>
						<hr>




						<!-- <table class=" table1 table">
						  <thead>
						    <tr>
						      <th scope="col">#</th>
						      <th scope="col">First</th>
						      <th scope="col">Last</th>
						      <th scope="col">Handle</th>
						    </tr>
						  </thead>
						  <tbody>
						    <tr>
						      <th scope="row">1</th>
						      <td>Mark</td>
						      <td>Otto</td>
						      <td>@mdo</td>
						    </tr>
						    <tr>
						      <th scope="row">2</th>
						      <td>Jacob</td>
						      <td>Thornton</td>
						      <td>@fat</td>
						    </tr>
						    <tr>
						      <th scope="row">3</th>
						      <td>Larry</td>
						      <td>the Bird</td>
						      <td>@twitter</td>
						    </tr>
						  </tbody>
						</table> -->

						
					</div>
					
				</div>
				
			</div>

			<div class="col-4">
				<div class="right">
					<img class="arrow" src="../assets/arrow.png">
					
				</div>
				
			</div>
			
		</div>
		
	</div>
	
</template>


<style scoped>

	hr{
		height: 1px;
		background-color:  #000000;
		width: 100%;

	}

	span{
		float: right;
		margin-right: 67px;
	}

	.wrapper{
		/*border: 1px solid green;*/
		height: 110vh;
		background-color:#EEF1F6;
	}

	.left{
		height: 94vh;
		/*border: 1px solid red;*/

	}

	.right{
		height: 94vh;
		/*border: 1px solid orange;*/
	}

	.inside{
		height: 94vh;
		/*border: 1px solid black;*/
		width: 123vh;
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
	}

	
</style>