<script setup>

import { onMounted, onUpdated, ref } from "vue";
import axios from "axios";

const testimonials = ref([]);

onMounted(async () => {
  const { data: fetchedTestimonials } = await axios.get("/data/testimonials.json");
  testimonials.value = fetchedTestimonials.testimonials;
});

onUpdated(() => {     

    $('.testimonial-carousel').owlCarousel({
		items: 1,
		margin: 30,
		dots: true,
		nav: false,
		loop: true,
		autoplay: true,
		responsiveClass: true,
		responsive: {
			575: {
				items: 1,
				nav: false,
				dots: false,
			},

			767: {
				items: 2,
				nav: false
			},

			990: {
				items: 2,
				loop: true,

			},
			1200: {
				items: 3,
				dots: true,
				loop: true,
			}
		}
	});

  
});

</script>


<template>
   <div class="project-bg">
	<div class="about-area section-padding">
 		<div class="container">
			<h1 class="h1-titulo" style="padding: 30px;">FAQ</h1>
			<p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minus sunt, deleniti <br>officia doloribus, quod adipisci enim, similique repellat omnis sed laborum.<br> Cupiditate labore molestiae asperiores quas cum. Temporibus, nemo tempore.</p>
 			<div class="row align-items-center">
 				<div class="col-lg-6 col-md-12 col-sm-12">
					<div class="about-img-wrap">
                    <div class="image-one wow fadeInUp" data-wow-delay=".2s" style="visibility: visible; animation-delay: 0.2s; animation-name: fadeInUp;">
                        <img src="/assets/img/bot.png" alt="">
						
                    </div>                        
                    <div class="image-two wow fadeInUp" data-wow-delay=".4s" style="visibility: visible; animation-delay: 0.4s; animation-name: fadeInUp;">
                        <!----img src="/assets/img/about/about-page-2.jpg" alt=""> ------>
                    </div>                                            
                </div> 					
 				</div>
 				<div class="col-lg-6 col-md-12 col-sm-12">
 					<div class="info-content-area">
 						<div class="section-title">
 							<!---h6>About Us</h6> --->
							
							 <h6 class="h1-mensaje1">Lorem ipsum dolor sit ament?</h6>
							 <!---span class="signo">^</span> --->
							 <h6 class="h1-mensaje2">Lorem ipsum dolor sit ament?</h6>
							 <!---span class="signo1">^</span> -->
							 <h6 class="h1-mensaje3">Lorem ipsum dolor sit ament?</h6>
							 <span class="signo2">^</span>
							 <h6 class="h1-mensaje4">Lorem ipsum dolor sit ament?</h6>
							 <h6 class="h1-mensaje5">Lorem ipsum dolor sit ament?</h6>
 						</div>
 						<!----div class="about-list-item mt-30">
							<p class="highlight">Since our launch in 1995, to deliver high value project.</p>
							<p class="highlight">We always provide flexible & quality task. </p>
							<p class="highlight">Uninque latest machinary used the industrial project.</p>
						</div> --->

 						<!----div class="row founded">
 							<div class="col-lg-4 col-md-6 col-12">
 								<div class="years"><span>25</span>Year of Success</div>
 							</div>
 							<div class="col-lg-8 col-md-6 col-12">
 								<div class="text">Since we established in 1995 experience &amp; still a growing protfolio day by day!</div>
 							</div>
 						</div> --->
 					</div>
 				</div>

 			</div>
 		</div>
 	</div>
   </div>
</template>

<style scoped>
@media (max-width: 767px) {
	img {
		position: relative;
		top: -90px;
		left: -40px;
	display: inline-block;
	max-width: 60%;
}
.h1-mensaje1{
	position: relative;
	width: 70%;
	top: -20px;
	left: 150px;
      padding: 20px;
	  color: #000;
	background-color: aliceblue;
}

}

img {
	display: inline-block;
	max-width: 60%;
}
.h1-titulo {
	color: beige;
	margin: 25px 0;
	padding: 50px 0; /* Ajusta el valor segÃºn tu preferencia */
	font-size: 60px;
}
p {
	font-family: 'Poppins', sans-serif;
	font-size: 16px;
	font-weight: 400;
	line-height: 25px;
	position: relative;
	top: -20px;
	left: 30px;
	color: beige;
}
.h1-mensaje1{
	position: relative;
	width: 70%;
	top: -210px;
	left: 150px;
      padding: 20px;
	  color: #000;
	background-color: aliceblue;
}

.h1-mensaje2{
	position: relative;
	width: 70%;
	top: -170px;
	left: 150px;
      padding: 20px;
	  color: #000;
	background-color: aliceblue;
}

.h1-mensaje3{
	position: relative;
	width: 70%;
	top: -130px;
	left: 150px;
      padding: 20px;
	  color: #000;
	background-color: aliceblue;
}
.h1-mensaje4{
	position: relative;
	width: 70%;
	top: -90px;
	left: 150px;
      padding: 20px;
	  color: #000;
	background-color: aliceblue;
}
.h1-mensaje5{
	position: relative;
	width: 70%;
	top: -50px;
	left: 150px;
      padding: 20px;
	  color: #000;
	background-color: aliceblue;
}
.signo {
            position: absolute;
            top: -180px;
            left: 460px;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #0070ff;
        }
		.signo1 {
            position: absolute;
            top: -80px;
            left: 460px;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #0070ff;
        }
		.signo2 {
            position: relative;
            top: -20px;
            left: 460px;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #0070ff;
        }

</style>






<!----div class="testimonial-area gray-bg section-padding">
	<div class="capricorn-testimonial">
		<div class="container">
			<div class="row">
				<div class="col-lg-12 text-center ">
					<div class="section-title">
						<h6>Testimonial</h6>
						<h2>Happy <b> Client </b>Says <br>About Us</h2>
					</div>
				</div>
			</div>

			<div class="row">
				<div class="col-lg-12">
					<div class="testimonial-carousel owl-carousel">
						<div class="single-team-item"
					   v-for="t in testimonials.slice(0,3)" :key="t.id"
					   >
							<div class="testimonial-icon"><i class="las la-quote-left"></i></div>
							<p>{{ t.content }}</p>
							<div class="testimonial-author">
							   <div class="testimonial-img">
								   <img :src="t.author_img" alt="">
							   </div>
							   <div class="author-info">
								   <h5>{{ t.author_name }}</h5><span>{{ t.author_designation}}</span>
							   </div>
						   </div>
						</div> 							
					</div>
				</div>
			</div>
		</div>
	</div>
</div>   ---->