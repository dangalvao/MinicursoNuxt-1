<template>
	<div>
		<headerUsuario/>
    	<div class="container pt-5">
	      <h1 class="mt-5 mb-4 text-center">Insira os dados da consulta</h1> 
	      <b-form @submit.prevent="onSubmit">

	        <b-form-group id="input-group-1" label="Data:" label-for="input-1">
	          <b-form-input
	            id="input-1"
	            v-model="form.d_consulta"
	            placeholder="Insira a data da consulta"
	            type="date"
	            required
	          ></b-form-input>
	        </b-form-group>

	        <b-form-group id="input-group-2" label="Veterinário:" label-for="input-2">
	        	<b-form-select 
	        		id="input-2"
	        		v-model="selected" 
	        		:options="options"
	        		required
	        	></b-form-select>
	        </b-form-group>

	        <b-button type="submit" variant="primary">Submit</b-button>
	      </b-form>
	    </div>
	</div>
</template>

<script>
export default {
  name: 'Pet',
  data(){
		return{
			selected: null,
			form: {
		        d_consulta: '',
		    },
		    options: [
		    	{value: null, text: "Escolha o veterinário para a consulta"}
		    	{value: 1, text: "Marcos"}
		    	{value: 2, text: "Heitor"}
		    	{value: 3, text: "Lucas"}
		    ]
		};
	},
	methods: {
		onSubmit(item){
	      console.log("Consulta feita!");
	    },
	}
}
</script>