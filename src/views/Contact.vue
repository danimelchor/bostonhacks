<template>
  <div class="container">
   	<div class="row">
	    <div class="col-sm contact-info">
    		<h1>Contact</h1>
	    	<div class="contact-info-item">
	    		<svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-telephone" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
				  <path fill-rule="evenodd" d="M3.654 1.328a.678.678 0 0 0-1.015-.063L1.605 2.3c-.483.484-.661 1.169-.45 1.77a17.568 17.568 0 0 0 4.168 6.608 17.569 17.569 0 0 0 6.608 4.168c.601.211 1.286.033 1.77-.45l1.034-1.034a.678.678 0 0 0-.063-1.015l-2.307-1.794a.678.678 0 0 0-.58-.122l-2.19.547a1.745 1.745 0 0 1-1.657-.459L5.482 8.062a1.745 1.745 0 0 1-.46-1.657l.548-2.19a.678.678 0 0 0-.122-.58L3.654 1.328zM1.884.511a1.745 1.745 0 0 1 2.612.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.678.678 0 0 0 .178.643l2.457 2.457a.678.678 0 0 0 .644.178l2.189-.547a1.745 1.745 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.634 18.634 0 0 1-7.01-4.42 18.634 18.634 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877L1.885.511z"/>
				</svg>
	    		<div class="contact-info-text"><p>(000)000-000</p></div>
	    	</div>
	    	<div class="contact-info-item">
	    		<svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-envelope" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
				  <path fill-rule="evenodd" d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1H2zm13 2.383l-4.758 2.855L15 11.114v-5.73zm-.034 6.878L9.271 8.82 8 9.583 6.728 8.82l-5.694 3.44A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.739zM1 11.114l4.758-2.876L1 5.383v5.73z"/>
				</svg>
	    		<div class="contact-info-text"><p>test@gmail.com</p></div>
	    	</div>
	    	<div class="contact-info-item">
	    		<svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-geo-alt" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
				  <path fill-rule="evenodd" d="M12.166 8.94C12.696 7.867 13 6.862 13 6A5 5 0 0 0 3 6c0 .862.305 1.867.834 2.94.524 1.062 1.234 2.12 1.96 3.07A31.481 31.481 0 0 0 8 14.58l.208-.22a31.493 31.493 0 0 0 1.998-2.35c.726-.95 1.436-2.008 1.96-3.07zM8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10z"/>
				  <path fill-rule="evenodd" d="M8 8a2 2 0 1 0 0-4 2 2 0 0 0 0 4zm0 1a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
				</svg>
	    		<div class="contact-info-text"><p>1000 Test Street</p><p>Floor 10</p><p>Boston, MA 02215</p></div>
	    	</div>
	    </div>
	    <div class="arrow-left"></div>
	    <div class="col-sm contact-form">
	    	<form @submit.prevent="sendEmail">
		    	<div class="input-group mb-3">
				  <div class="input-group-prepend">
				    <span class="input-group-text" id="basic-addon1">
				    	<svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-person-fill" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
						  <path fill-rule="evenodd" d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
						</svg>
					</span>
				  </div>
				  <input v-model="name" type="text" class="form-control" placeholder="Full name" aria-label="Full name" aria-describedby="basic-addon1">
				</div>
		      	<div class="input-group mb-3">
				  <div class="input-group-prepend">
				    <span class="input-group-text" id="basic-addon1">
				    	<svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-envelope-fill" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
					  		<path fill-rule="evenodd" d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555zM0 4.697v7.104l5.803-3.558L0 4.697zM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757zm3.436-.586L16 11.801V4.697l-5.803 3.546z"/>
						</svg>
					</span>
				  </div>
				  <input v-model="email" type="text" class="form-control" placeholder="Email address" aria-label="Email address" aria-describedby="basic-addon1">
				</div>
		      	<div class="input-group">
				  <div class="input-group-prepend">
				    <span class="input-group-text">
				    	<svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-chat-left-fill" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
						  <path fill-rule="evenodd" d="M2 0a2 2 0 0 0-2 2v12.793a.5.5 0 0 0 .854.353l2.853-2.853A1 1 0 0 1 4.414 12H14a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2H2z"/>
						</svg>
				    </span>
				  </div>
				  <textarea v-model="message" class="form-control" aria-label="With textarea" placeholder="Message"></textarea>
				</div>
		      <input type="submit" class="btn btn-primary btn-lg" value="Submit">
		    </form>
	    </div>
	  </div>
  </div>
</template>

<style lang="scss" scoped>
$main-green : #88e3c5;

.container {
	border-radius: 5px;
	border: 1px solid #111;
	margin-top: 2vw;
	width: 60vw;

	.contact-info {
		padding: 2vw;
		font-size: 1.2em;

		h1 {
			font-size: 2.8em;
			font-weight: bold;
			color: #444;
			margin-bottom: 2vw;
		}

		.contact-info-item {
			margin-top: 30px;

			svg {
				display: inline-block;
				margin-right: 10px;
				vertical-align: top;
			}

			.contact-info-text {
				display: inline-block;
				p {
					margin-bottom: 10px;
				}
			}
		}
	}

	.contact-form {
		padding: 2vw;
		background-color: $main-green;
		border-radius: 0 5px 5px 0;

		input:focus, textarea:focus {
			box-shadow: none;
			font-weight: bold;
			border-color: #444;
		}

		input[type="submit"] {
			margin-top: 20px;
		}

		textarea {
			min-height: 15vh;
		}
	}
}

.arrow-left {
	width: 0; 
	height: 0;
	margin-top: 30px; 
	border-top: 40px solid transparent;
	border-bottom: 40px solid transparent; 
  
	border-right:40px solid $main-green; 
}

@media (max-width: 1200px) {
  .container {
  	width: 100vw;
  	max-width: 100vw;
  	border: 0 none;
  	border-top: 1px solid #111;
  	border-bottom: 1px solid #111;
  	border-radius: 0;
  	margin: 0;

  	.contact-form {
  		border-radius: 0;
  	}
  }
}

@media (max-width: 600px) {
  .container {
  	border: 0 none;
  	margin-top: 14vw;

  	.contact-info {
  		h1 {
	  		font-size: 2.2em;
	  	}
  	}

  	.col-sm {
  		display: block;
		padding: 7vw;
  	}

  	.arrow-left {
		width: 0; 
	  	height: 0; 
	  	border-left: 40px solid transparent;
	  	border-right: 40px solid transparent;
	  	margin-left: 30px;
	  	margin-top: -40px;
	  
		border-bottom:40px solid $main-green; 
	}
  }
}
</style>

<script>
import emailjs from 'emailjs-com';

export default {
  name: "Contact",
  data() {
  	return {
  		name: '',
  		email: '',
  		message: ''
  	}
  },
  methods: {
    sendEmail(e) {
      console.log('Sent');

      try {
        emailjs.sendForm('service_qvqtmgy', 'template_t1gw5po', e.target,
        'user_IZVUqnSg9iT7KANzDWV86', {
          name: this.name,
          email: this.email,
          message: this.message
        })

      } catch(error) {
          console.log({error})
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  }
};
</script>
