<template>
  <div class="row">

    <!-- coluna 1 -->
    <div class="col-8">

      <h2>Filmes</h2>

      <ul class="list-group list-group-flush">

        <FilmesListaIten 
          v-for="filme in filmes"
          :key="filme.id"
          class="tema-escuro"
          v-bind="filme"
        />

      </ul>
    </div>

    <!-- coluna 2 -->
    <div class="col-4">

      <FilmesListaItenInfo/>

    </div>

  </div>
</template>

<script>

import FilmesListaIten from './FilmesListaIten.vue'
import FilmesListaItenInfo from './FilmesListaItenInfo.vue'

export default {
  components: {
    FilmesListaIten,
    FilmesListaItenInfo
  },

  data(){
    return {
      filmes: [
        { id: 1, titulo: 'Vingadores: Guerra Infinita', ano: 2023, diretor: 'Stan Lee' },
        { id: 2, titulo: 'Homem Formiga e a Vespa', ano: 2023, diretor: 'Stan Lee' },
        { id: 3, titulo: 'Pantera Negra', ano: 2023, diretor: 'Stan Lee' },
        { id: 4, titulo: 'Deadpool 2', ano: 2023, diretor: 'Stan Lee' }
      ]
    }
  }
}
</script>
