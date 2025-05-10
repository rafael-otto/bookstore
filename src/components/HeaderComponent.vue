<template>
    <header>
        <RouterLink to="/"><div class="logotipo">
            <h1>IFbooks</h1>
            <hr>
            <h3>Apreço a<br>leitura</h3>
        </div></RouterLink>
        <div class="barrapesquisa">
            <input type="text" name="pesquisar" id="pesquisar" placeholder="Pesquisar">
            <button><img src="../../public/header-img/Search.png" alt="botão de pesquisa"></button>
        </div>
        <div class="opcoes">
            <ul>
                <li>Termos</li>
                <li>Equipe</li>
                <li>Envio</li>
                <li>Devoluções</li>
            </ul>
        </div>
        <div class="direcionamentos">
            <ul>
                <li>
                    <RouterLink to="/cart"><img src="../../public/header-img/Icon.png"
                            alt="icone de direcionamento para o carrinho de compras"></RouterLink>
                </li>
                <hr>
                <li>
                    <a href=""><img src="../../public/header-img/Icon2.png"
                            alt="icone de direcionamento para os produtos favoritos"></a>
                </li>
                <hr>
                <li>
                    <a href=""><img src="../../public/header-img/Icon3.png"
                            alt="icone de direcionamento para a página do usuário"></a>
                </li>
            </ul>
        </div>
    </header>
</template>
<style scoped>
header {
    padding: 1vw 6vw 1vw 6vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 1vw;
    border-bottom: 1px solid #27AE60;
}
/*Logotipo*/
.logotipo {
    display: flex;
    align-items: center;
}
.logotipo h1 {
    padding-right: 0.5vw;
    font-size: 1.3rem;
    color: black;
}
.logotipo hr {
    border: 1px solid #27AE60;
    height: 35px;
}
.logotipo h3 {
    padding-left: 0.5vw;
    color: rgba(39, 174, 96, 0.6);
}
/*Pesquisar*/
.barrapesquisa input,
.barrapesquisa button {
    border: none;
    cursor: pointer;
}
.barrapesquisa input {
    background-color: #f1f1f1;
    padding: 0.6vw 10vw 0.6vw 1vw;
    font-size: 1.1rem;

}
.barrapesquisa ::placeholder {
    color: #b8b8b8;
}
.barrapesquisa button {
    background-color: #00000000;
    transform: translate(-2.5vw, 0.35vw);
    }
/*Opções*/
.opcoes ul {
    display: flex;
}
.opcoes ul li {
    color: #7B7881;
    padding: 0 4vw 0 0;
    font-size: 1.2rem;
    cursor: pointer;
}
/*Direcionamentos*/
.direcionamentos ul {
    display: flex;
}
.direcionamentos ul li {
    padding: 0 1.3vw 0 1.3vw;
}
.direcionamentos hr {
    border: 1px solid #27AE60;
    height: 20px;
}
.direcionamentos ul li img {
    height: 1.5vw;
}
</style>
