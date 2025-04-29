<script setup>
import { ref, reactive } from 'vue';
import Books from './components/Books.vue';
import BookProgress from './components/BookProgress.vue';
import AddBook from './components/AddBook.vue';

let books = reactive([
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
]);

function addBook(newBook) {
  newBook.id = Math.max(...books.map(el => el.id)) + 1;
  books.push(newBook);
  showAddBook.value = false;
}

let showAddBook = ref(false);

function toggleIsRead(id) {
  books.forEach((book) => {
    if (book.id === id) {
      book.isRead = !book.isRead;
    }
  })
}
</script>

<template>
  <div v-if="!showAddBook" class="container">
    <h1>📖 Meus Livros</h1>

    <div class="header-btns">
      <button
        class="btn"
        @click="showAddBook = true"
      >
        Adicionar Livro +
      </button>
    </div>
 
    <div class="books-container">
      <Books @toggleIsRead="toggleIsRead" :books="books"/>

      <BookProgress :books="books"/>
    </div>
  </div>

  <div v-else class="container">
    <AddBook @addBook="addBook" @closeAddBook="showAddBook = false"/>
  </div>
</template>

<style scoped>

</style>
