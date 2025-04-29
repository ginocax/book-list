<script setup>
import Books from './components/Books.vue';

let books = [
  {
    id: 1,
    title: "History of Europe",
    cover:
      "https://m.media-amazon.com/images/I/811WfBrMtWL._AC_UF1000,1000_QL80_.jpg",
    isRead: true,
    isbn: "0-395-07157-8",
    author: "Simon Janekins",
  },
  {
    id: 2,
    title: "Penguin Classics",
    cover:
      "https://m.media-amazon.com/images/I/91cKrZxBuwL._AC_UF1000,1000_QL80_.jpg",
    isRead: false,
    isbn: "0-395-07157-8",
    author: "Henry Eliot",
  },
  {
    id: 3,
    title: "Becoming",
    cover:
      "https://m.media-amazon.com/images/I/81KGjsBXQ7L._AC_UF1000,1000_QL80_.jpg",
    isRead: false,
    isbn: "0-395-07157-8",
    author: "Michelle Obama",
  },
  {
    id: 4,
    title: "Sonnets",
    cover:
      "https://m.media-amazon.com/images/I/715hva4FrAL._UF894,1000_QL80_.jpg",
    isRead: false,
    isbn: "0-395-07157-8",
    author: "Sthephen Fry",
  },
];
</script>

<template>
  <div class="container">
    <h1>📖 Meus Livros</h1>
    <div class="header-btns">
      <button
        class="btn"
        
      >
        Adicionar Livro +
      </button>
    </div>
 
    <div class="books-container">
      <Books :books="books"/>
    </div>
  </div>
</template>

<style scoped>

</style>
