<template>
 <div class="container">
  	<div class="row">
  		<div class="col">
  			<h1>Calculator - Testing (Currently displaying McDonalds in the US)</h1>
	    	<p>Type your most recent meal and look at your carbon footprint based on that meal</p>
	    	<p>For more information on how to reduce it, <router-link to="/alternatives">click here</router-link></p>
  		</div>
  		<div class="col" id="formDiv">
  			<div class="input-group mb-3">
			  <div class="input-group-prepend">
			    <span class="input-group-text" id="basic-addon1"><i class="fas fa-drumstick-bite"></i></span>
			  </div>
			  <input v-model="foodSearch" type="text" class="form-control" placeholder="Type a food... (Current: burger)" aria-label="Food" aria-describedby="basic-addon1">
			  <div class="input-group-append">
			    <button class="btn btn-outline-secondary" type="button" id="button-addon2"><i class="fas fa-search"></i></button>
			  </div>
			</div>
  		</div>
  	</div>
  	<div class="row map"><Map /></div>
 </div>
</template>

<style lang="scss" scoped>
$main-green : #88e3c5;

.container {
	width: 60vw;

	h1 {
		font-size: 2.8em;
		font-weight: bold;
		color: #444;
	}

	p {
		display: block;
		line-height: 1.3em;
		font-size: 1.1em;
		margin-top: 15px;
	}

	.col {
		margin-top: 4vw;

		.input-group {
			width: 20vw;
			float: right;

			input {
				border-color: #bbb;
			}

			.btn, .input-group-text {
				background-color: #eee;
				border-color: #bbb;
			}

			.btn:hover {
				color: #111;
			}

			.btn:focus, input:focus {
				box-shadow: inset 0px 0px 0px 1px $main-green;
				border-color: $main-green;
				font-weight: bold;
				box-sizing: border-box;
			}
		}
	}
}

.map {
	height: 30vw;
	border: 1px solid #111;
	border-radius: 5px;
	margin: 5vh auto;
}

@media (max-width: 1200px) {
  .row {
  	padding: 1.5vw 5vw;
  }

  .container {
  	width: 100vw;
  	max-width: 100vw;
  	padding: 0;

  	.col .input-group {
  		width: 30vw;
  	}
  }

  .map {
  	height: 100%;
  	border-radius: 0;
  	width: 100vw;
  	margin: 0;
  	padding: 0;
  	margin-top: 4vw;
  }
}

@media (max-width: 600px) {
	.container {
		margin-top: 14vw;
		padding-top: 10vw; 

		.row {
			margin-bottom: 10vw;
		}

		.col .input-group {
			width: 90vw;
		}
	}

	.map {
		height: 100%;
	  	width: 100vw;
	}
}
</style>

<script>
import Map from "@/components/map.vue";

export default {
  name: "Calculator",
  components: {
    Map
  },
  data() {
  	return {
  		foodSearch: ''
  	}
  }
};
</script>
