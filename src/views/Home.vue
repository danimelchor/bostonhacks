<template>
  <div class="container">
  	<div class="info-home-container">
  		<div class="info-home">
	  		<h1>FoodPrint</h1>
	  		<p>Calculate your individual carbon footprint in a click</p>
	  		<router-link to="/calculator">Calculate mine!</router-link >
  		</div>
  	</div>
  	<img src="@/assets/img/slide1.png">
  </div>
</template>

<style lang="scss" scoped>
$main-green : #88e3c5;

.container {
	position: relative;
	padding: 0;
	width: 60vw;

	img {
		display: block;
		width: 60vw;
	}

	.info-home-container {
		background: rgba(0,0,0,0.7);
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

@media (max-width: 1200px) {
  .container {
  	width: 100vw;
  	max-width: 100vw;

  	img {
  		width: 100vw;
  	}

  	.info-home-container {
  		width: 100vw;

  		.info-home {
		  	a {
		  		width: 20vw;
		  	}
		}
  	}
  }
}

@media (max-width: 600px) {
	.container {
		margin-top: 14vw;
		height: 32vh;

		img {
			height: 32vh;
		}

		.info-home-container {
			position: absolute;

			.info-home {
				left: 5%;
				width: 90vw;

				h1 {
					font-size: 2.2em;
				}

				p {
					font-size: 1.3em;
				}

				a {
					width: 100%;
					padding: 4vw 0;
				}
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
