<template>
    <div class="container">
        <div class="description">
            <div class="show-info">
                <h4>Gabinet wsparcia psychologicznego <br>Daniel Szczepanek</h4>
                <!-- <p>Rajskie Ziółko</p> -->
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
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2499.7012694302!2d16.154064315758877!3d51.206155979586704!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x470f128fc67cb129%3A0x63bddf8a17943570!2sDziennikarska%205A%2C%2059-220%20Legnica!5e0!3m2!1spl!2spl!4v1649769012869!5m2!1spl!2spl" width="800" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
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