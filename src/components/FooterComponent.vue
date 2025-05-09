<template>
    <footer>
        <div class="geral">
            <div class="social">
                <p>IFbooks</p>
                <ul>
                    <li>
                        <a href="#"><img src="../../public/footer-img/facebook.png" alt=""></a>
                    </li>
                    <li>
                        <a href="#"><img src="../../public/footer-img/instagram.png" alt=""></a>
                    </li>
                    <li>
                        <a href="#"><img src="../../public/footer-img/twitter.png" alt=""></a>
                    </li>
                </ul>
            </div>
            <div class="about">
                <div class="contact">
                    <p>Contato</p>
                    <ul>
                        <li>
                            <img src="../../public/footer-img/telephone.png" alt="">
                            <p>+55 47 40045263</p>
                        </li>
                        <li>
                            <img src="../../public/footer-img/clock.png" alt="">
                            <p>8h às 23h - Seg a Sex</p>
                        </li>
                        <li>
                            <img src="../../public/footer-img/mail.png" alt="">
                            <p>contato@ifbooks.com</p>
                        </li>
                    </ul> 
                </div>
                <ul class="payment">
                    <li>
                        <img src="../../public/footer-img/paypal.png" alt="">
                    </li>
                    <li>
                        <img src="../../public/footer-img/mastercard.png" alt="">
                    </li>
                    <li>
                        <img src="../../public/footer-img/visa.png" alt="">
                    </li>
                </ul>
            </div>
        </div>
        <hr>
        <p class="copyright">&copy; Alguns direitos reservados. IFbooks 2025.</p>
    </footer>
</template>
<style scoped>
/*GERAL*/
footer {
    background-color: #27AE60;
    color: white;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
}
.geral {
    display: flex;
    justify-content: space-between;
    padding: 3vw 6vw 2vw 6vw;
}
/*SOCIAL*/
.geral .social p {
    padding-bottom: 1vw;
}
.geral .social ul {
    display: flex;
}
.geral .social ul li {
    padding-right: 1vw;
}
/*ABOUT*/
.geral .about .contact p:first-child{
    font-weight: 900;
}
.geral .about .contact ul li{
    display: flex;
    padding-top: 1vw;
}
.geral .about .contact ul li img {
    padding-right: 1vw;
}
.geral .about .payment {
    display: flex;
    padding-top: 4vw;
}
.geral .about .payment li {
    padding-right: 1vw;
}
/*COPYRIGHT*/
.copyright {
    font-size: 1.1rem;
    color: rgba(255, 255, 255, 0.60);
    text-align: center;
    padding: 2vw;
}
</style>