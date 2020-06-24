<template>
	<section>

		<div class="container">

			<HcodeSectionNewsIndividual 
				v-for="notice in news"
				:key="notice.id"
				:img-name="notice.img"
				:img-info="notice.imgInfo"
				:news-date="notice.date"
			>

			<template #title>
				<h2>{{ notice.title }}</h2>
			</template>

			<p>{{ notice.content  | truncate(200) }}</p>

			</HcodeSectionNewsIndividual>

		</div>

	</section>
</template>

<script>	
	import HcodeSectionNewsIndividual from './HcodeSectionNewsIndividual'
	export default{
		components:{
			HcodeSectionNewsIndividual
		},
		data(){
			return{
				news:[]
			}
		},
		created(){
			this.news = [
				{
					id: 1,
					title: 'Começaram os treinos p/ a nova temporada',
					content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestiae nostrum nisi, repudiandae illum perferendis! Eveniet id ullam, corporis tenetur doloribus, et nostrum voluptas sequi, dolorum laborum sit iusto explicabo odio. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Obcaecati nemo, inventore numquam quasi nostrum at fugiat dolor officiis quas vero eligendi odio dolorem placeat consectetur ab, repudiandae incidunt dicta doloribus.',
					date: '2020-02-01',
					img: 'original (2).jpg',
					imgInfo: 'Noticia 1'
				},
				{
					id: 2,
					title: "Jogo de quarta-feira termina empatado",
					content: "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
					date: "2020-02-03",
					img: "original (3).jpg",
					imgInfo: "Noticia 2"
				},
				{
					id: 3,
					title: "A inauguração do novo estádio será na semana que vem",
					content: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Suscipit similique reiciendis porro! Architecto sed sequi error animi debitis modi explicabo veniam sint, quia consequatur, iusto impedit harum iure! Aspernatur, deserunt?",
					date: "2020-06-30",
					img: "original (4).jpg",
					imgInfo: "Noticia 3"
				}
			]
		}
	}	
</script>

<style scoped>
	section{
		padding: 50px 0;
		margin-top: 25px;
		background-color: #f37520;
	}
</style>