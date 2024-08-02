<script setup>
import { onMounted, ref } from "vue";
import axios from "axios";

const projects = ref([]);

onMounted(async () => {
  const { data: fetchedProjects } = await axios.get("/data/projects.json");
  projects.value = fetchedProjects.projects;
});


</script>

<template>
   <div class="project-bg">
	<div class="container">
	<form action="procesar_registro.php" method="post">
            <input type="text" class="form-control mb-2" id="inlineFormInput" placeholder="Nombre completo:" required>
            <input type="text" class="form-control" id="inlineFormInputGroup" placeholder="Correo electrónico" required>
			<input type="text" class="form-control mb-2" id="inlineFormInput" placeholder="Teléfono:" required>
            <input type="text" class="form-control mb-2" id="inlineFormInput" placeholder="Empresa:" required>
            <textarea id="mensaje" name="mensaje" rows="4" placeholder="Mensaje (opcional):"></textarea>
            
            <button type="submit">COMIENZA AHORA</button>
        </form>
</div>
   </div>
</template>

<style scoped>

@media (max-width: 767px) {
	.container {
            max-width: 10px; /* Ajusta el ancho máximo según tus preferencias */
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 10px;
        }
        input, textarea, button {
            width: 100%;
            padding: 10px;
			color: #000;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #007BFF;
            color: #fff;
            cursor: pointer;
        }
}

  .container {
            max-width: 1200px; /* Ajusta el ancho máximo según tus preferencias */
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 10px;
        }
        input, textarea, button {
            width: 100%;
            padding: 10px;
			color: #000;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
			text-align: center;
			width: 30% ;
            background-color: #fff;
            color: #007BFF;
            cursor: pointer;
			display: block;
			margin: 0 auto;
        }
</style>
















  <!---iv class="container">
 			<div class="offset-lg-2 col-lg-8 text-center">
 				<div class="section-title">
 					<h6>Recent Project</h6>
 					<h2>Brilliant <b>Ideas</b> With
 						<br>Excellent <b>Work </b></h2>
 					<p>Industrial equipment modern technique sit amet, consectetur adipisicing elit. <br> Repellendus laboriosam omnis cum.</p>
 				</div>
 			</div>
 			<div class="row mt-60">
 				<div class="col-lg-4 col-md-6 col-12"
				 v-for="(project, i) in projects" :key="project.id"
				>
 					<div class="single-project-item bg-cover"
					 :class="i === 0 ? 'project-bg' : `project-bg-${i + 1}`"
					>
 						<div class="project-inner">
 							<router-link :to="{name:'project-details'}" class="project-icon">
 								<i class="las la-plus"></i>
 							</router-link>
 							<div class="hover-info">
 								<h6>{{ project.tag }}</h6>
 								<h4>{{ project.title }}</h4>
 							</div>
 						</div>
 					</div>
 				</div>
 			</div>
 		</div>
 	</div> ------>