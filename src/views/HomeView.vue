<script setup>
const produtos = [
    {
        id: 1,
        titulo: 'Chain of Iron: Volume 2',
        autor: 'Cassandra Clare',
        preco: 23.24,
        capa: 'https://placehold.co/600x400.png',
    },
    {
        id: 2,
        titulo: 'Chain of Thorns',
        autor: 'Cassandra Clare',
        preco: 23.24,
        capa: 'https://placehold.co/600x400.png',
    },
    {
        id: 3,
        titulo: 'City of Fallen Angels',
        autor: 'Cassandra Clare',
        preco: 13.94,
        capa: 'https://placehold.co/600x400.png',
    },
    {
        id: 4,
        titulo: 'Nona the Ninth',
        autor: 'Cassandra Clare',
        preco: 16.84,
        capa: 'https://placehold.co/600x400.png',
    },
    {
        id: 5,
        titulo: 'Harlem Shuffle',
        autor: 'Colson Whitehead',
        preco: 26.92,
        capa: 'https://placehold.co/600x400.png',
    },
    {
        id: 6,
        titulo: 'Two Old Women',
        autor: 'Velma Wallis',
        preco: 13.95,
        capa: 'https://placehold.co/600x400.png',
    },{
        id: 7,
        titulo: 'Carrie Soto Is Back',
        autor: 'Taylor Jenkins Reid',
        preco: 26.04,
        capa: 'https://placehold.co/600x400.png',
    },{
        id: 8,
        titulo: 'Book Lovers',
        autor: 'Emily Henry',
        preco: 15.81,
        capa: 'https://placehold.co/600x400.png',
    },
];
</script>

<template>
  <main>
    <section class="banner">
      <div class="autorMes">
        <p>Autor de Abril</p>
      </div>
      <div class="text">
        <h1>Eric-Emanuel Schmitt</h1>
        <p>Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions, and in 2001 he received the title of Chevalier des Arts et des Lettres. His books have been translated into over 40 languages.</p>
        <div class="button">
        <button>Acessar página do livro</button>
      </div>
      </div>

      <div class="image">
        <img src="" alt="Livro">
      </div>
    </section>
    <section class="barraCentral">
      <ul>
        <li>
          <span><font-awesome-icon icon="fa-solid fa-truck" /></span>
          <p>Frete grátis para SC</p>
        </li>
        <li>
          <span><font-awesome-icon icon="fa-solid fa-star" /></span>
          <p>Livros recomendados</p>
        </li>
        <li>
          <span><font-awesome-icon icon="fa-solid fa-book-open" /></span>
          <p>Mais vendidos</p>
        </li>
      </ul>
    </section>
    <section class="books">
      <h2>Lançamentos</h2>
      <div v-for="book in produtos" :key="book.id" class="book">
        <img src="" alt="">
        <p class="title">{{ book.titulo }}</p>
        <p class="autor">{{ book.autor }}</p>
        <p class="price">R$ {{ book.preco }}</p>
        <button><span><font-awesome-icon icon="fa-solid fa-cart-shopping" /></span>Comprar</button>
      </div>
    </section>

  </main>
</template>

<style scoped>

</style>
