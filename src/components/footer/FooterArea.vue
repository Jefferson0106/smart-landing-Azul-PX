<template>
    <footer class="footer-area">
 		<div class="container">
 			<div class="footer-up">
 				<div class="row gy-5">
 					<div class="col-lg-3 col-md-6 col-sm-12">
 						<div class="logo">
 							<img src="/assets/img/logo-blanco.png" alt="dustrian-logo">
 						</div>
 						<!---p>We are the leaders in the building <br> construction and factories. We’re <br> around over the worldwide. </p> ---->
 					
 					</div>
 					<div class="col-lg-2 offset-lg-1 col-md-6 com-sm-12">
 						<h5>dolorisit</h5>
 						<ul>
 							<li>
 								<router-link :to="{name:'about'}">Lorem</router-link>
 								<router-link :to="{name:'project'}">Ipsum</router-link>
 								<router-link to="/">Ament</router-link>
 							</li>
 						</ul>
 					</div>
 					<div class="col-lg-3 col-md-6 col-sm-12">
 						<h5>Legal</h5>
 						<ul>
 							<li>
 								<router-link :to="{name:'service-details'}"><span>-</span> Politica De Privacida</router-link>
 								<router-link :to="{name:'service-details'}"><span>-</span> Termino De Uso</router-link>
 							</li>
 						</ul>
 					</div>
 					<div class="col-lg-3 col-md-6">
 						<div class="subscribe-form">
							<div>
 							<div class="social-area">
 							<a href=""><i class="lab la-facebook-f"></i></a>
 							<a href=""><i class="lab la-instagram"></i></a>
 							<a href=""><i class="lab la-twitter"></i></a>
 							<a href=""><i class="la la-skype"></i></a>
							</div>
 						</div>
 						</div>
 					</div>
 				</div>
 			</div>
 		</div>
 	</footer>
</template>