<template>
  <div id="app">
  	{{ nome }}
    <lv-addtarefa></lv-addtarefa>
    <lv-busca></lv-busca>
    <lv-tarefas></lv-tarefas>
  </div>
</template>

<script>

import LvAddtarefa from './AddTarefa.vue'
import LvTarefas from './Tarefas.vue'
import LvBusca from './Busca.vue'
import {mapState} from 'vuex'

export default {
  name: 'app',
  components: {LvAddtarefa, LvTarefas, LvBusca},
  computed: {
  	...mapState(['nome'])
  }
}
</script>

