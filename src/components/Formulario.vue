<script setup>
const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>

<template>
    <form @submit.prevent="cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="tarefaTemp" @input="editaTarefaTemp" required type="text"
                    placeholder="Digite a descrição da tarefa" class="form-control">
            </div>
            <div class="col-md-1">
                <button type="submit" class="btn btn-primary">Enviar</button>
            </div>
            <div class="col-md-2">
                <select @change="trocarFiltro" class="form-control">
                    <option value="todas">Todas tarefas</option>
                    <option value="pendentes">Pendentes</option>
                    <option value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>