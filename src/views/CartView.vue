<script setup>
import { ref } from 'vue';

const frete = ref(0);

const livros = ref([
    {
        id: 1,
        img: "",
        titulo: "Chain of Iron: Volume 2",
        autor: "Cassandra Clare",
        preco: 23.24,
        quantidade: 0,
        capa: 'https://m.media-amazon.com/images/I/81IP261kwlL._AC_UF1000,1000_QL80_.jpg',
    },
    {
        id: 2,
        img: "",
        titulo: "Chain of Thorns",
        autor: "Cassandra Clare",
        preco: 46.48,
        quantidade: 0,
        capa: 'https://m.media-amazon.com/images/I/91298Zw5GdL._AC_UF1000,1000_QL80_.jpg',
    }
]);
</script>
<template>
    <div class="about">
      <h1>Carrinho</h1>
    </div>
    <section class="table" v-for="(livro, id) in livros" :key="id">
      <table>
        <thead>
          <tr>
            <th>Título</th>
            <th>Quantidade</th>
            <th>Subtotal</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>
              <img :src="livro.capa" alt="">
              <div>
                <h3>{{ livro.titulo }}</h3>
                <p>{{ livro.autor }}</p>
                <p>R$ {{ livro.preco }}</p>
              </div>
            </td>
            <td style="display: flex;">
              <button v-if="livro.quantidade>0"  @click="livro.quantidade--">-</button>
              <button v-else>-</button>
              <p>{{ livro.quantidade }}</p>
              <button @click="livro.quantidade++">+</button>
            </td>
            <td>R$ {{ (livro.preco * livro.quantidade).toFixed(2) }}</td>
          </tr>
        </tbody>
      </table>
    </section>
    <router-link to="/" exact><button>Voltar pra loja</button></router-link>
    <section style="display: flex;">
      <div>
        <input type="text">
        <button>Inserir Cupom</button>
      </div>
      <div id="total" style="border: 1px solid black;">
        <h3>Total da Compra</h3>
        <ul v-for="(livro, id) in livros" :key="id">
          <li>
            <p>Produtos: {{ (livro.preco * livro.quantidade).toFixed(2) }}</p>
          </li>
          <li>
            <p v-if="frete == 0">Frete: GRÁTIS</p>
            <p v-else>Frete: {{ frete }}</p>
          </li>
          <li>
            <p>Total: R$ {{ (livro.preco * livro.quantidade + frete).toFixed(2) }}</p>
          </li>
        </ul>
        <button>Ir para o pagamento</button>
      </div>
    </section>
  </template>
  <style scoped>
    thead {
      border-bottom: 1px solid #27AE60;
    }
  </style>
