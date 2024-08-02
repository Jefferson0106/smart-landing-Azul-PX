<script setup>

import { onMounted, ref, onUpdated } from 'vue'

import axios from "axios";

const services = ref([]);

onMounted(async () => {
  const { data: fetchedServices } = await axios.get("/data/services.json");
  services.value = fetchedServices.services;
});

onUpdated(() => {     

		// Service Slider    
        $(".service-slider").owlCarousel({
		loop: true,
		items: 3,
		dots: true,
		nav: false,
		smartSpeed: 1000,
		autoHeight: false,
		touchDrag: true,
		mouseDrag: true,
		margin: 30,
		autoplay: true,
		slideSpeed: 600,
		responsive: {
			0: {
				items: 1,
				nav: false,
				dots: false,
			},
			600: {
				items: 2,
				nav: false,
				dots: false,
			},
			768: {
				items: 2,
				nav: false,
				dots: false,
			},
			1100: {
				items: 3,
				nav: false,
				dots: true,
			}
		}
	});
  
});

</script>

<template>
   <div class="hero-area-bg-2">
	<div class="container">
			
 			<div class="row align-items-center">
 				<div class="col-lg-6 col-md-12 col-sm-12">
					<div class="about-img-wrap">
                    <div class="image-one wow fadeInUp" data-wow-delay=".2s" style="visibility: visible; animation-delay: 0.2s; animation-name: fadeInUp;">
						<h2><span class="punto"></span>Gestiona tus productos y servicios</h2>
						<p>We are build construction site lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea enim et, similique minus soluta ipsum dolor sit, amet consectetur adipisicing elit.</p>
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
							 <img src="/assets/img/boxes2.png" alt="">
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
</template>

<style scoped>
@media (max-width: 767px) {
	.hero-area-bg-2 h2{
		position: absolute;
		top: -77px;
	/*	padding-left: 35px; */
		font-size: 15px; /* Tamaño en píxeles */
		color: #0070ff;
		
	}
	.hero-area-bg-2 p{
	position: absolute;
	top: -67px;
	padding: 20px;
}
img {
	display: inline-block;
	max-width: 70%;
}
}
</style>



 <!-----div class="services-area gray-bg section-padding pad-bot-90">
 		<div class="container">
 			<div class="row">
 				<div class="offset-lg-2 col-lg-8 text-center">
 					<div class="section-title">
 						<h6>Services</h6>
 						<h2>Providing the Best Global <b>Industry Services</b></h2>
 					</div>
 				</div>
 			</div>

 			<div class="row mt-30">
 				<div class="col-lg-12">
 					<div class="service-slider owl-carousel">
 						<div class="single-service-area"
						v-for="service in services.slice(0,6)" :key="service.id"
						>
 							<div class="service-icon">
 								<i :class="service.icon"></i>
 							</div>
 							<h5>{{ service.title }}</h5>
 							<p>{{ service.content }}</p>
 							<router-link :to="{name:'service-details'}" class="read-more">Read More</router-link>
 						</div> 						
 					</div>
 				</div>
 			</div>
 		</div>
 	</div>  ---->

