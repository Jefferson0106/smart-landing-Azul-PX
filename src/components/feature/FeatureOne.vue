<script setup>

import { onMounted, ref} from 'vue'

import axios from "axios";

const features = ref([]);

onMounted(async () => {
  const { data: fetchedFeatures } = await axios.get("/data/features.json");
  features.value = fetchedFeatures.features;
});


</script>

<template>
  <div class="about-area section-padding">
 		<div class="container">
 			<div class="row align-items-center">
 				<div class="col-lg-6 col-md-12 col-sm-12">
					<div class="about-img-wrap">
                    <div class="image-one wow fadeInUp" data-wow-delay=".2s" style="visibility: visible; animation-delay: 0.2s; animation-name: fadeInUp;">
                        <img src="/assets/img/bank-card-mobile-phone-online-payment.jpg" alt="">
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
							 <h2><span class="punto"></span>Automatiza Proceso De Pago</h2>
 						</div>
 						<p>We are build construction site lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea enim et, similique minus soluta ipsum dolor sit, amet consectetur adipisicing elit.</p>
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
    img {
		position: relative;
		top: -50px;
	display: inline-block;
	max-width: 70%;
}
.info-content-area .section-title h2{
	position: absolute;
	top: 10px;
	left: -40px;
/*	padding-left: 35px; */
	font-size: 5px; /* Tamaño en píxeles */
	color: #0070ff;
	white-space: nowrap;
}
.info-content-area .section-title p{
	position: absolute;
	top: -1px;
	left: -90px;
	padding: 20px;
}
}
.info-content-area .section-title h2{
	position: absolute;
	top: -100px;
	left: -40px;
/*	padding-left: 35px; */
	font-size: 30px; /* Tamaño en píxeles */
	color: #0070ff;
	white-space: nowrap;
}
.info-content-area .section-title p{
	position: absolute;
	top: -67px;
	left: -90px;
	padding: 20px;
}
</style>


 <!-----div class="feature-area section-padding"> 
 		<div class="container">
 			<div class="row">
 				<div class="col-lg-6 col-md-12 col-sm-12">
 					<div class="section-title">
 						<h6>Features</h6>
 						<h2> We manage & organized Quality <b>Industrial</b> Project</h2>
 					</div>
 					<div class="single-feature-item"
					v-for="feature in features.slice(0,3)" :key="feature.id"
					>
 						<div class="feature-icon">
 							<i :class="feature.icon"></i>
 						</div>
 						<div class="feature-content">
 							<h5>{{ feature.title }}</h5>
 							<p>{{ feature.content }}</p>
 						</div>
 					</div> 					
 				</div>
 				<div class="col-lg-6 col-md-12 col-sm-12">
 					<div class="feature-image">
 						<img src="/assets/img/feature/feature.png" alt="">
 					</div>
 				</div>
 			</div>
 		</div>
 	</div> ----->