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
    capa: 'https://m.media-amazon.com/images/I/91CwkPkZhuL._AC_UF1000,1000_QL80_.jpg',
  },
  {
    id: 3,
    titulo: 'City of Fallen Angels',
    autor: 'Cassandra Clare',
    preco: 13.94,
    capa: 'https://m.media-amazon.com/images/I/81KL1LCy4bL._UF894,1000_QL80_.jpg',
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
    capa: 'https://i1.sndcdn.com/artworks-fQ60tDlGfNtr1Uub-z208aw-t1080x1080.jpg',
  },
  {
    id: 6,
    titulo: 'Two Old Women',
    autor: 'Velma Wallis',
    preco: 13.95,
    capa: 'https://www.harpercollins.com/cdn/shop/files/9780063394711_65e9ebef-3f04-4be2-89a9-eeae3878073b_1200x1200.jpg?v=1715175769',
  },
  {
    id: 7,
    titulo: 'Carrie Soto Is Back',
    autor: 'Taylor Jenkins Reid',
    preco: 26.04,
    capa: 'https://m.media-amazon.com/images/I/91EBzb6utDL.jpg',
  },
  {
    id: 8,
    titulo: 'Book Lovers',
    autor: 'Emily Henry',
    preco: 15.81,
    capa: 'https://m.media-amazon.com/images/I/71Xy4AL7jKL.jpg',
  },
]
</script>

<template>
  <main>
    <section class="banner">
      <div class="text">
        <div class="autorMes">
          <p>Autor de Abril</p>
        </div>
        <h1>Eric-Emanuel Schmitt</h1>
        <p class="descricao">
          Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions, and in 2001 he received the title of Chevalier des Arts et des Lettres. His books have been translated into over 40 languages.
        </p>
        <div>
          <button class="buttonBanner">Acessar página do livro</button>
        </div>
      </div>

      <div class="image">
        <img
          src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgNM-WgqLF_HtYa8xUec1vEU-q4KQbHi9tgac-1WG5-cir6NZ-qG6NquQE3WBdwDZyEsF7Jp4uRd_KwZhVnyUn_3AGWeUoFUk8UWt8LOsXLBx_b6R5aMiKpsNZlVoiWciWyx1CyeGN972c/s640/Schmitt_Nocognia_3D.jpg"
          alt="Livro">
        <p>*within the stock limit</p>
      </div>
    </section>
    <section class="barraCentral">
      <ul>
        <li>
          <span><img src="../../public/home-img/Truck.png" alt="truck"></span>
          <p>Frete grátis para SC</p>
        </li>
        <li class="meio">
          <span><img src="../../public/home-img/Star.png" alt="star"></span>
          <p>Livros recomendados</p>
        </li>
        <li>
          <span><img src="../../public/home-img/Book-open.png" alt="Book Open"></span>
          <p>Mais vendidos</p>
        </li>
      </ul>

    </section>
    <section class="books">
      <div>
        <h2>Lançamentos</h2>
      </div>
      <div class="tabela">
        <div v-for="livro in produtos" :key="livro.id" class="livro">
          <img :src="livro.capa" alt="">
          <p class="titulo">{{ livro.titulo }}</p>
          <p class="autor">{{ livro.autor }}</p>
          <p class="preco">R$ {{ livro.preco }} <img src="../../public/home-img/favorite.png" alt="Coração"></p>
          <button class="botaoComprar">
            <img src="../../public/home-img/cart.png" alt="comprar">
            <p>Comprar</p>
          </button>
        </div>
      </div>
    </section>
  </main>
</template>
<style scoped>
main {

  .banner {
    margin: 1vw 6vw 1vw 6vw;
    display: flex;

    .text {
      h1 {
        font-size: 3.5rem;
        font-weight: 900;
        margin-top: 2vw;
        margin-bottom: 2vw;
      }

      p.descricao {
        margin-right: 15vw;
      }

      .autorMes {
        margin-top: 3vw;
        padding: 0.5vw 0.3vw 0.5vw 0.3vw;
        border: 1px solid #27AE60;
        width: 10vw;
        text-align: center;

        p {
          color: #27AE60;
          font-size: 1.1rem;
        }
      }


        button.buttonBanner {
          margin-top: 3vw;
          padding: 1vw 1.5vw;
          font-size: 1.1rem;
          color: white;
          border: none;
          background-color: #27AE60;
          cursor: pointer;
        }

        button.buttonBanner:hover {
          background-color: #219752;
        }
    }

    .image {
      p {
        text-align: right;
      }

    }
  }

  .barraCentral {

    padding: 3vw 0 3vw 0;
    border-bottom: 1px solid #27AE60;
    border-top: 1px solid #27AE60;
    width: 100%;

    ul {
      list-style: none;
      display: flex;
      justify-content: space-around;

      li {
        display: flex;
        align-items: center;

        p {
          font-size: 1.5rem;
          font-weight: 600;
          margin-left: 1vw;
        }
      }

      li.meio {
        border-right: 1px solid #27AE60;
        border-left: 1px solid #27AE60;
        padding: 0 8vw 0 8vw
      }
    }
  }

  .books {
    margin: 1vw 6vw 1vw 6vw;

    h2 {
      font-size: 2.5rem;
      font-weight: 600;
      color: #27AE60;
      margin: 3vw 0 3vw 0;
    }

    .tabela {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;

      .livro {
        display: grid;

        img {
          height: 28vw;
          width: 20vw;
        }

        .titulo {
          font-size: 1.5rem;
          padding: 1vw 0 1vw 0;
          font-weight: 700;
        }

        .autor {
          color: #4F4C57;
          padding-bottom: 0.2vw;
        }

        .preco {
          font-weight: 700;
          margin-bottom: 0.6vw;
          font-size: 1.4rem;
          img {
            transform: translate(12vw, 0.35vw);
            height: 1.9vw;
            width: auto;
            cursor: pointer;
          }
        }

        button.botaoComprar {
          margin-top: 1vw;
          margin-bottom: 2vw;
          padding: 0.8vw 1.2vw;
          font-size: 1.1rem;
          color: white;
          border: none;
          background-color: #27AE60;
          cursor: pointer;
          display: flex;
          justify-content: center;
          align-items: center;
          gap: 0.5vw;
        }

        button.botaoComprar img {
          height: 1.2vw;
          width: auto;
        }

        button.botaoComprar p {
          font-size: 1.3rem;
          margin: 0;
        }

        button.botaoComprar:hover {
          background-color: #219752;
        }
      }
    }
  }
}
</style>
