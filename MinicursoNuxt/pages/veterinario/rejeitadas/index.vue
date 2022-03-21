<template>
	<div>
		<HeaderVeterinario/>
		<div class="container pt-5">
      <div class="mx-auto mt-5">
      	<h1 class="mt-5 mb-4 text-center"> Consultas rejeitadas</h1>
        <b-table striped hover :items="items" :fields="fields">
          <template #cell(Ações)="row">
            <b-button size="sm" @click="aceitarConsulta(row.item)" class="mr-2">
              Aceitar consulta
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
        { pet: 'Billy', data: '2022-12-28', estado: 'Rejeitada', veterinario_responsável: 'Marcos' }
      ]
    }
  },
  methods: {
    aceitarConsulta(row){
      console.log("Consulta aceita!");
    }
  }
}
</script>