<template>
    <header>
        <div class="logotipo">
            <h1>IF Books</h1>
            <hr>
            <h3>Apreço a<br>leitura</h3>
        </div>
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
                    <a href=""><img src="../../public/header-img/Icon.png"
                            alt="icone de direcionamento para o carrinho de compras"></a>
                </li>
                <li>
                    <a href=""><img src="../../public/header-img/Icon2.png"
                            alt="icone de direcionamento para os produtos favoritos"></a>
                </li>
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
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    margin: 1vw 5vw 1vw 5vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
/*Logotipo*/
.logotipo {
    display: flex;
    align-items: center;
}
.logotipo h1 {
    padding-right: 0.5vw;
}
.logotipo hr {
    border: 1px solid #27AE60;
    height: 32px;
}
.logotipo h3 {
    padding-left: 0.5vw;
    color: rgba(39, 174, 96, 0.6);
}
/*Pesquisar*/
.barrapesquisa {
    padding-left: 5vw;
}
.barrapesquisa input,
.barrapesquisa button {
    border: none;
}
.barrapesquisa input {
    background-color: #f1f1f1;
    padding: 0.4vw 5vw 0.4vw 0.4vw;
    font-size: 1.1rem;

}
.barrapesquisa ::placeholder {
    color: #b8b8b8;
}
.barrapesquisa button {
    background-color: #00000000;
    transform: translate(-2vw, 0.35vw);
    }
</style>
