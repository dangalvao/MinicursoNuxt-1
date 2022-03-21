<template>
	<div>
		<headerUsuario/>
    	<div class="container pt-5">
			<h3 class="mt-4 mb-2"><nuxt-link to="/usuario/pets/">
			Voltar aos pets</nuxt-link></h3>
			<hr>
			<div class="mt-3 mb-5 ml-2 mr-2">
				<b-row>
					<b-col>
						<b-row class="mt-2">
							<b-col>
								<h1 class="pt-2">Pandora</h1> 
							</b-col>
						</b-row>
						<b-row>
							<b-col class="mt-1 mb-1" cols="12">
								<span><strong>Aniversário: </strong>22-02-2016</span>
							</b-col>
						</b-row>
						<b-row>
							<b-col class="mt-1 mb-1" cols="12">
								<span><strong>Dono: </strong>Pandora</span>
							</b-col>
						</b-row>
						<b-row>
							<b-col class="mt-1 mb-1" cols="12">
								<b-button size="sm" class="mr-2":to="/usuario/pets/consulta/1">
					              Solicitar consulta
					            </b-button>
					            <b-button size="sm" variant="warning" class="mr-2" :to="/usuario/pets/edit/1">
					              Editar
					            </b-button>
					            <b-button size="sm" variant="danger" @click="excluir" class="mr-2">
					              Excluir
					            </b-button>
							</b-col>
						</b-row>
					</b-col>
				</b-row>
			</div>
		</div>
	</div>
</template>

<script>
export default {
  name: 'Pet',
  methods: {
    excluir(){
      console.log("Pet excluido");
    }
  }
}
</script>