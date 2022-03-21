<template>
	<div>
		<HeaderVeterinario/>
		<div class="container pt-5">
	      <div class="mx-auto mt-5">
	      	<h1 class="mt-5 mb-4 text-center"> Consultas aceitas</h1>
	        <b-table striped hover :items="items" :fields="fields">
            <template #cell(Ações)="row">
              <b-button size="sm" @click="rejeitarConsulta(row.item)" class="mr-2">
                Rejeitar consulta
              </b-button>
            </template> 
          </b-table>
	      </div>
	    </div>
	</div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      fields: ['pet', 'data', 'estado', 'veterinário', 'Ações'],
      items: [
        { pet: 'Pandora', data: '2022-04-15', estado: 'Aceita', veterinario_responsável: 'Heitor' },
        { pet: 'Scooby', data: '2022-09-04', estado: 'Aceita', veterinario_responsável: 'Heitor' },
      ]
    }
  },
  methods: {
    recusarConsulta(row){
      console.log("Consulta rejeitada!");
    }
  }
}
</script>