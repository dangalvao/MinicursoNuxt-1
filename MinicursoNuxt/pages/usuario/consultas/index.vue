<template>
	<div>
		<HeaderUsuario/>
		<div class="container pt-5">
	      <div class="mx-auto mt-5">
	      	<h1 class="mt-5 mb-4 text-center"> Consultas solicitadas</h1>
	        <b-table striped hover :items="items"></b-table>
	      </div>
	    </div>
	</div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
      return {
        items: [
          { pet: 'Mel', data: '2022-03-10', estado: 'Em aberto', veterinario_responsável: 'Marcos' },
          { pet: 'Pandora', data: '2022-04-15', estado: 'Aceita', veterinario_responsável: 'Heitor' },
          { pet: 'Scooby', data: '2022-09-04', estado: 'Aceita', veterinario_responsável: 'Heitor' },
          { pet: 'Billy', data: '2022-12-28', estado: 'Rejeitada', veterinario_responsável: 'Marcos' }
        ]
      }
    }
}
</script>