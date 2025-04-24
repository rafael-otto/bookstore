<script setup>
const produtos = [
    {
        id: 1,
        titulo: 'Chain of Iron: Volume 2',
        autor: 'Cassandra Clare',
        preco: 23.24,
        capa: 'https://m.media-amazon.com/images/I/81IP261kwlL._AC_UF1000,1000_QL80_.jpg',
    },
    {
        id: 2,
        titulo: 'Chain of Thorns',
        autor: 'Cassandra Clare',
        preco: 23.24,
        capa: 'https://m.media-amazon.com/images/I/91298Zw5GdL._AC_UF1000,1000_QL80_.jpg',
    },
    {
        id: 3,
        titulo: 'City of Fallen Angels',
        autor: 'Cassandra Clare',
        preco: 13.94,
        capa: 'https://m.media-amazon.com/images/I/815MzJpG6iL._AC_UF1000,1000_QL80_.jpg',
    },
    {
        id: 4,
        titulo: 'Nona the Ninth',
        autor: 'Cassandra Clare',
        preco: 16.84,
        capa: 'https://m.media-amazon.com/images/I/81a2wDWhyNL._AC_UF1000,1000_QL80_.jpg',
    },
    {
        id: 5,
        titulo: 'Harlem Shuffle',
        autor: 'Colson Whitehead',
        preco: 26.92,
        capa: 'https://scottsemegran.com/images/stories/book_reviews/harlem_shuffle_by_colson_whitehead.jpg',
    },
    {
        id: 6,
        titulo: 'Two Old Women',
        autor: 'Velma Wallis',
        preco: 13.95,
        capa: 'https://m.media-amazon.com/images/I/81Yo0MecUrL.jpg',
    },
    {
        id: 7,
        titulo: 'Carrie Soto Is Back',
        autor: 'Taylor Jenkins Reid',
        preco: 26.04,
        capa: 'https://m.media-amazon.com/images/I/916WmQau7IL.jpg',
    },
    {
        id: 8,
        titulo: 'Book Lovers',
        autor: 'Emily Henry',
        preco: 15.81,
        capa: 'https://m.media-amazon.com/images/I/71Xy4AL7jKL.jpg',
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
        <img src="https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1724071848i/32572089.jpg" alt="Livro">
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
        <img :src="book.capa" alt="">
        <p class="title">{{ book.titulo }}</p>
        <p class="autor">{{ book.autor }}</p>
        <p class="price">R$ {{ book.preco }}</p>
        <button><span><font-awesome-icon icon="fa-solid fa-cart-shopping" /></span>Comprar</button>
      </div>
    </section>
  </main>
</template>
