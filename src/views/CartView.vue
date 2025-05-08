<script setup>
import { ref, computed } from 'vue'

const frete = ref(0)

const livros = ref([
  {
    id: 1,
    img: '',
    titulo: 'Chain of Iron: Volume 2',
    autor: 'Cassandra Clare',
    preco: 23.24,
    quantidade: 0,
    capa: 'https://m.media-amazon.com/images/I/81IP261kwlL._AC_UF1000,1000_QL80_.jpg',
  },
  {
    id: 2,
    img: '',
    titulo: 'Chain of Thorns',
    autor: 'Cassandra Clare',
    preco: 46.48,
    quantidade: 0,
    capa: 'https://m.media-amazon.com/images/I/91298Zw5GdL._AC_UF1000,1000_QL80_.jpg',
  },
])

const texto = ref('')

const total = computed(() => {
  return livros.value.reduce((total, livro) => total + livro.preco * livro.quantidade, 0)
})

const desconto = computed(() => {
  let subtotal = livros.value.reduce((total, livro) => total + livro.preco * livro.quantidade, 0)
  return texto.value.toLowerCase() == 'lrv10' ? subtotal - subtotal * 0.1 : subtotal
})
</script>
<template>
  <main>
    <h1>Carrinho</h1>
    <section class="table" >
      <table>
        <thead>
          <tr >
            <th>Título</th>
            <th>Quantidade</th>
            <th>Subtotal</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(livro, id) in livros" :key="id">
            <td>
              <div class="livro">
                <img :src="livro.capa" alt="" />
                <div class="infos">
                  <h3>{{ livro.titulo }}</h3>
                  <p style="font-size: small;">{{ livro.autor }}</p>
                  <p style="font-weight: 600;">R$ {{ livro.preco }}</p>
                </div>
              </div>
            </td>
            <td style="align-items: center;">
              <div class="button">
                <button v-if="livro.quantidade > 0" @click="livro.quantidade--">-</button>
                <button v-else>-</button>
                <p>{{ livro.quantidade }}</p>
                <button @click="livro.quantidade++">+</button>
              </div>
            </td>
            <td>
              <p class="preco">R$ {{ (livro.preco * livro.quantidade).toFixed(2) }}</p>
            </td>
          </tr>
        </tbody>
      </table>
    </section>
    <router-link to="/" exact><button>Voltar pra loja</button></router-link>
    <section style="display: flex">
      <div>
        <input type="text" v-model="texto" />
        <button type="submit">Inserir Cupom</button>
      </div>
      <div id="total" style="border: 1px solid black">
        <h3>Total da Compra</h3>
        <ul>
          <li>
            <p>Produtos: R$ {{ total.toFixed(2).replace('.', ',') }}</p>
          </li>
          <li>
            <p v-if="frete == 0">Frete: GRÁTIS</p>
            <p v-else>Frete: {{ frete }}</p>
          </li>
          <li>
            <p>Total: R$ {{ desconto.toFixed(2).replace('.', ',') }}</p>
          </li>
        </ul>
        <a href="https://www.mercadopago.com.br/pix/home#from-section=menu"
          ><button>Ir para o pagamento</button></a
        >
      </div>
    </section>
  </main>
</template>
<style scoped>
main {
  margin: 10vw 5vw 10vw 5vw;
}
h1 {
  color: #27ae60;
  font-size: 2.5rem;
  font-weight: 500;
  margin-bottom: 2vw;
}
table{
  border-collapse: collapse;
  margin: 0 auto;
  width: 90vw;
  height: 30vw;
}
/*table tr{
  border: 1px solid green!important;
}*/
thead {
  /*tr {
    color: blueviolet;
  }*/
  th {
    font-weight: bold;
    border-bottom: 1px solid #27ae60;
  }
}
tbody {  
  /*border: 1px solid green!important;*/
  tr td {
    border-bottom: 1px solid #c4c4c4;
  }
  img {
    margin: 1vw;
    height: 6vw;
    width: 4vw;
  }
  .livro {
    display: flex;
    padding: 1vw 0 1vw 0;
    div {
      padding: 1vw 14vw 0 0;
    }
    div h3 {
      font-weight: 500;
      font-family: 0.3rem;
    }
  }
  .button {
    display: flex;
    border: 1px solid black;
    justify-content: center;
    align-items: center;
    height: 3vw;
    button {
      background-color: white;
      border: none;
      padding: 0 1.5vw 0 1.5vw;
      cursor: pointer;
    }
  }
  .preco {
    padding-left: 17vw;
    padding-right: 5vw;
    font-weight: 700;
    font-size: 1.1rem;
  }
}
</style>