<template>
	<div>
		<li v-for="tarefa in tarefas">
			<lv-deltarefa :tarefa="tarefa"></lv-deltarefa>
			{{ tarefa }}
		</li>
	</div>
</template>

<script>

import LvDeltarefa from './DelTarefa.vue'

import {mapGetters} from 'vuex'

export default{
	name: 'lv-tarefas',
	components: {LvDeltarefa},
	computed:{
		...mapGetters({
			tarefas: 'listaTarefas'
		})
	}
}

	
</script>