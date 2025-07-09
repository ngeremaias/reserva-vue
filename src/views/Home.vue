<template>
  <div class="fractal">
  <div class="fr-1"></div>
  <div class="fr-2"></div>
  <div class="fr-3"></div>
  <div class="fr-4"></div>
  <div class="fr-5"></div>
</div>
  <div class="center">
    <div class="text">
      <h1><strong>Espaços Esportivos</strong> ao seu alcance!</h1>
      <div class="subtitle">
        📍 <h2>Encontre o lugar ideal para sua pelada!</h2>
      </div>
    </div>

    <form @submit.prevent="buscar">
      <div class="search-box">
        <input type="text" v-model="busca" placeholder="Pesquisar por espaços esportivos..." />
        <select v-model="cidade">
          <option value="">Brasil</option>
          <option v-for="uf in ufs" :key="uf">{{ uf }}</option>
        </select>
        <button type="submit">🔍</button>
      </div>
    </form>

    <div class="tags">
      <span class="tag" v-for="tag in tags" :key="tag">{{ tag }}</span>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'


const busca = ref('')
const cidade = ref('')
const tags = [
  'Quadra de futsal', 'Quadra de vôlei', 'Campo de futebol',
  'Quadra de basquete', 'Quadra de tênis',
  'Mais próximos', 'Mais baratos', 'Bem avaliados'
]
const ufs = [
  'AC', 'AL', 'AP', 'AM', 'BA', 'CE', 'DF', 'ES', 'GO',
  'MA', 'MT', 'MS', 'MG', 'PA', 'PB', 'PR', 'PE', 'PI',
  'RJ', 'RN', 'RS', 'RO', 'RR', 'SC', 'SP', 'SE', 'TO'
]

function buscar() {
  alert(`Buscando por "${busca.value}" em "${cidade.value || 'Brasil'}"`)
}
</script>

<style src="../assets/css/variables.css"></style>
<style src="../assets/css/index.css"></style>