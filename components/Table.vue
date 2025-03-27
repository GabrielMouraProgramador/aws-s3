<template>
  <VCard flat class="border" rounded="xl">
    <VDataTable show-select :headers="headers" :items="files" item-value="id">
      <template v-slot:item.nome="{ item }">
        <div class="d-flex aling-center">
          <v-icon size="25" v-if="item.type === 'Pasta'" color="warning"
            >mdi-folder-outline</v-icon
          >
          <v-icon size="25" v-else-if="item.type === 'PDF'" color="blue"
            >mdi-file-document-outline</v-icon
          >
          <v-icon size="25" v-else-if="item.type === 'Imagem'" color="green"
            >mdi-image-outline</v-icon
          >
          <span class="ml-1 my-auto">
            {{ item.name }}
          </span>
        </div>
      </template>

      <template v-slot:item.acoes>
        <VBtn icon="mdi-pencil" variant="tonal" size="35" class="me-2" color=""> </VBtn>
        <VBtn icon="mdi-delete" variant="tonal" size="35" color="red"></VBtn>
      </template>
    </VDataTable>
  </VCard>
</template>

<script setup>
import { ref } from "vue";

const headers = ref([
  { title: "Nome", key: "nome" },
  { title: "Tipo", key: "type" },
  { title: "Data Modificação", key: "date" },
  { title: "Tamanho", key: "size" },
  { title: "Ações", key: "acoes", sortable: false },
]);

const files = ref([
  { id: 1, name: "Documentos", type: "Pasta", date: "10/06/2023 14:30", size: "-" },
  { id: 2, name: "Relatório.pdf", type: "PDF", date: "08/06/2023 09:15", size: "2.4 MB" },
  { id: 3, name: "Banner.jpg", type: "Imagem", date: "05/06/2023 16:42", size: "1.8 MB" },
  { id: 4, name: "Projetos", type: "Pasta", date: "01/06/2023 11:20", size: "-" },
]);
</script>
<style scoped>
.border {
  border: solid black 1px;
}
</style>
