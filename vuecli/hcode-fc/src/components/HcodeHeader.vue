<template>
	<div>
		<header>
			<div class="container">
				<nav class="navbar navbar-expand">
					
					<a href="" class="link navbar-brand mr-auto">
						<img src="./../assets/logo.svg" alt="Hcode" class="img d-inline-block align-top" id="logo"> Futebol Clube
					</a>

					<div class="links mr-2">
						
						<a 
						href="" 
						@click.prevent="$emit('change-component', 'home')"
						class="btn mr5">Inicio</a>

						<a href="" @click.prevent="$emit('change-component', 'news')" class="btn mr5">Notícias</a>

						<a 
						href=""
						class="btn mr5"
						@click.prevent="$emit('change-component', 'home')"
						>Classificações</a>

						<select name="championship" id="sel-champ" class="form-control" @change="$emit('sel-championship', $event.target.value)">

							<option value="Campeonato Brasileiro" selected>
							Campeonato Brasileiro</option>

							<option value="Campeonato Espanhol">Campeonato Espanhol</option>

							<option value="Campeonato Inglês">Campeonato Inglês</option>

							<option value="Campeonato Italiano">Campeonato Italiano</option>

						</select>

					</div>

				</nav>
			</div>
		</header>
	</div>
</template>

<script>
	export default{

	}
</script>

<style scoped>
	header{
		background-color: #000;
	}
	#logo{
		width: 150px;
		height: 100%;
	}
	.links{
		display: inline-flex;
	}
	.links a{
		color: #fff
	}
	.links a:focus{
		outline: none!important;
		box-shadow: none!important;
	}
	.link{
		color: #d48e23;
		font-size: 30px;
		font-family: Rajdhani;
	}
</style>