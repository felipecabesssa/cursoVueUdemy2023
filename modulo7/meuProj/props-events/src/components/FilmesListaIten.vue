<template>
    <li class="list-group-item">
        <span>{{ filmeTituloConcatenado }}</span>
        <button class="btn btn-success float-right">Editar</button>
    </li>
</template>

<script>
export default {
  props: {
    filmeTitulo: {
      type: String,
      // required: true,
      default() {
        return 'Vingadores'
        // essa forma com o default como função usamos quando é array
        // quando for um tipo simples podemos usar conforme abaixo
      }, 
      // default: 'Vingadores'
      validator(filmeTitulo) {
        return filmeTitulo.includes('Marvel')
        // verifica se tem 'Marvel' no titulo do filme 
      }
    }
  },
  computed: {
    filmeTituloConcatenado() {
      return `Título: ${this.filmeTitulo}`
    }
  },
  created() {
    console.log(typeof this.filmeTitulo);
  }
}
</script>
