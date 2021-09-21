<template>
  <q-card-section>
        <div class="text-h6">Exemplo 1</div>
        <div class="text-subtitle2">Dashboard / Exemplo 1</div>
      </q-card-section>
  <div class="q-pa-md">
    <q-table
      title="Filtro"
      :rows="rows"
      :columns="columns"
      row-key="name"
    />
  </div>
</template>

<script>
const columns = [
  {
    name: 'situacao',
    required: true,
    label: 'Situação',
    align: 'left',
    field: row => row.situacao,
    format: val => `${val}`,
    sortable: true
  },
  { situacao: 'codExemplo', align: 'center', label: 'Cod Exemplo', field: 'codExemplo', sortable: true },
  { situacao: 'nome', align: 'center', label: 'Nome', field: 'nome' },
  { situacao: 'descricao', align: 'center', label: 'Descrição', field: 'descricao' },
  { situacao: 'origem', align: 'center', label: 'Origem', field: 'origem' },
  { situacao: 'contato', align: 'center', label: 'Contato', field: 'contato' },
  { situacao: 'email', align: 'center', label: 'E-mail', field: 'email' },
  { situacao: 'telefone', align: 'center', label: 'Telefone 1', field: 'telefone' },
  { situacao: 'telefoneSegundo', align: 'center', label: 'Telefone 2', field: 'telefoneSegundo' }
]

const rows = [
  {
    situacao: 'Em aberto',
    codExemplo: 565,
    nome: 'nome 15',
    descricao: 'Descrição 15',
    origem: 'Origem 15',
    contato: 'contato 15',
    email: 'email 15',
    telefone: 'Telefone 15',
    telefoneSegundo: 'Telefone 15'
  },
  {
    situacao: 'Em aberto',
    codExemplo: 237,
    nome: 'nome 20',
    descricao: 'Descrição 20',
    origem: 'Origem 20',
    contato: 'contato 20',
    email: 'email 20',
    telefone: 'Telefone 20',
    telefoneSegundo: 'Telefone 20'
  },
  {
    situacao: 'Em aberto',
    codExemplo: 262,
    nome: 'nome 17',
    descricao: 'Descrição 17',
    origem: 'Origem 17',
    contato: 'contato 17',
    email: 'email 17',
    telefone: 'Telefone 17',
    telefoneSegundo: 'Telefone 17'
  },
  {
    situacao: 'Finalizado',
    codExemplo: 305,
    nome: 'nome 11',
    descricao: 'Descrição 11',
    origem: 'Origem 11',
    contato: 'contato 11',
    email: 'email 11',
    telefone: 'Telefone 11',
    telefoneSegundo: 'Telefone 11'
  },
  {
    situacao: 'Finalizado',
    codExemplo: 356,
    nome: 'nome 14',
    descricao: 'Descrição 14',
    origem: 'Origem 14',
    contato: 'contato 14',
    email: 'email 14',
    telefone: 'Telefone 14',
    telefoneSegundo: 'Telefone 14'
  },
  {
    situacao: 'Finalizado',
    codExemplo: 375,
    nome: 'nome 19',
    descricao: 'Descrição 19',
    origem: 'Origem 19',
    contato: 'contato 19',
    email: 'email 19',
    telefone: 'Telefone 19',
    telefoneSegundo: 'Telefone 19'
  },
  {
    situacao: 'Em aberto',
    codExemplo: 392,
    nome: 'nome 18',
    descricao: 'Descrição 18',
    origem: 'Origem 18',
    contato: 'contato 18',
    email: 'email 18',
    telefone: 'Telefone 18',
    telefoneSegundo: 'Telefone 18'
  },
  {
    situacao: 'Em aberto',
    codExemplo: 408,
    nome: 'nome 12',
    descricao: 'Descrição 12',
    origem: 'Origem 12',
    contato: 'contato 12',
    email: 'email 12',
    telefone: 'Telefone 12',
    telefoneSegundo: 'Telefone 12'
  },
  {
    situacao: 'Em aberto',
    codExemplo: 452,
    nome: 'nome 10',
    descricao: 'Descrição 10',
    origem: 'Origem 10',
    contato: 'contato 10',
    email: 'email 10',
    telefone: 'Telefone 10',
    telefoneSegundo: 'Telefone 10'
  },
  {
    situacao: 'Em aberto',
    codExemplo: 518,
    nome: 'nome 16',
    descricao: 'Descrição 16',
    origem: 'Origem 16',
    contato: 'contato 16',
    email: 'email 16',
    telefone: 'Telefone 16',
    telefoneSegundo: 'Telefone 16'
  }
]

export default {
  setup () {
    return {
      columns,
      rows
    }
  }
}
</script>
