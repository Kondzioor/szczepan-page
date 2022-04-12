<template>
    <div class="container">
        <div class="description">
            <div class="show-info">
                <h4>Sklep stacjonarny:</h4>
                <p>Rajskie Ziółko</p>
                <p>ul. Neptuna 15</p>
                <p>59-220 Legnica</p>
            </div>
            <div class="contact-info">
                <h4>Kontakt</h4>
                <p>telefon: +48 506755369</p>
                <p>poniedziałek-piątek godz. 9.00 - 17.00</p>
                <p>sobota godz. 10.00 - 14.00</p>
            </div>
        </div>
<iframe class="map-item" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2499.6450864434623!2d16.187940715382375!3d51.20719114043015!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x470f0d65fa4e2bff%3A0x8cb310319c319b8d!2sRajskie%20Zi%C3%B3%C5%82ko%20-%20Sklep%20zielarsko%20medyczny!5e0!3m2!1spl!2spl!4v1644265415493!5m2!1spl!2spl" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
    </div>
</template>
<style scoped>
.container{
    display: flex;
    align-items: center;
    padding: 30px;
}
.description{
    display: flex;
    flex-direction: column;
}
.show-info,
.contact-info{
    margin: 15px;
}
.map-item{
    flex-grow: 1;
}
@media (max-width: 700px){
    .container{
        flex-direction: column;

    }
}
</style>