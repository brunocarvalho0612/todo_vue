<script setup>
  const props = defineProps (['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>

<template>
  <form @submit.prevent="props.cadastraTarefa">
      <div class="row">
        <div class="col row">
          <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required type="text" placeholder="Digite a descrição da sua tarefa">
        </div>
        <div class="col-md-2">
          <button class="btn btn-primary" type="submit">Cadastrar</button>
        </div>
        <div class="col-md-2">
          <select @change="props.trocarFiltro" class="form-control">
            <option value="todas">Todas Tarefas</option>
            <option value="pendentes">Tarefas Pendentes</option>
            <option value="finalizadas">Tarefas Finalizadas</option>
          </select>
        </div>
      </div>
    </form>
</template>
