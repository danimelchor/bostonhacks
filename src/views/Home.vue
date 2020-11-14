<template>
  <div class="container">
  	<div class="info-home-container">
  		<div class="info-home">
	  		<h1>FoodPrint</h1>
	  		<p>Calculating your individual carbon footprint in a click</p>
	  		<a href="/calculator">Calculate mine!</a>
  		</div>
  	</div>
  	<img src="@/assets/img/slide1.png">
  </div>
</template>

<style lang="scss" scoped>
$main-green : #88e3c5;

.container {
	position: relative;
	width: 60vw;

	img {
		display: block;
		width: 60vw;
	}

	.info-home-container {
		background: rgba(0,0,0,0.4);
		width: 60vw;
		height: 100%;
		position: absolute;
		top: 0;

		.info-home {
			top: 50%;
			left: 10%;
			transform: translateY(-50%);
			position: absolute;
			display: block;
			color: white;

			h1 {
				color: white;
				font-size: 4em;
				position: relative;
				margin-bottom: 15px;
				font-weight: bold;
			}

			p {
				color: white;
				font-size: 1.5em;
			}

			a {
				padding: 1vw;
				background-color: transparent;
				border: 1px solid white;
				border-radius: 5px;
				color: white;
				font-size: 1.1em;
				text-decoration: none;	
				display: block;
				width: 10vw;
				text-align: center;
				margin-top: 15%;
			}
		}
	}
}
</style>

<script>
export default {
  name: "Home"
};
</script>
