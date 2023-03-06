<template>
    <section class="footer">
        <div class="social">

            <a href="https://www.facebook.com/psychologLegnicaLubin"><i class="fab fa-facebook" ></i></a>
        </div>
        <ul class="list">
            <li @click="homePush" >
                <a href="/">Główna</a>
            </li>
            <li>
                <a href="/about">O mnie</a>
            </li>
            <li>
                <a href="/contact">Kontakt</a>
            </li>
        </ul>
        <p class="copyright">Gabinet wsparcia psychologicznego Daniel Szczepanek @ 2022 v1.0 by <a href="http://www.rajskieziolko.pl">Rajskie Ziółko</a></p>
    </section>
</template>
<script>
export default {
    methods:{
        homePush() {
        this.router.push('/');
      },
    }
}
</script>
<style scoped>
.footer{
    padding: 40px 0;
    background-color: #fff;
    border-top: 2px solid #5b250a;
    margin-top: 10px;
}
.footer .social{
    text-align: center;
    padding-bottom: 25px;
    color: #4b4c4d;
}
.footer .social a{
    font-size: 24px;
    color:inherit;
    border: 1px solid #ccc;
    width: 40px;
    height: 40px;
    line-height: 40px;
    display: inline-block;
    text-align: center;
    border-radius: 50%;
    margin: 0 8px;
    opacity: 0.75;
}
.footer .social a:hover{
    opacity:0.9;
    color: rgb(81,167,38);
    border-color: rgb(81,167,38);
}
.footer ul{
    margin-top: 0;
    margin-bottom: 0;
    padding: 0;
    list-style: none;
    font-size: 18px;
    line-height: 1.6;
    text-align: center;
}
.footer ul li a{
    color: inherit;
    text-decoration: none;
    opacity: 0.8;
}
.footer ul li{
    display: inline-block;
    padding: 0 15px;
}
.footer ul li a:hover{
    opacity: 1;
    color: rgb(81,167,38);
    border-color: rgb(81,167,38);
}
.footer .copyright{
    margin-top: 15px;
    text-align: center;
    font-size: 13px;
    color: #aaa
}
</style>