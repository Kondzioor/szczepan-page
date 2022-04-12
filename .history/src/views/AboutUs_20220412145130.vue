<template>
<div class="container">
        <section>
            <img src="../assets/boy.jpg" alt="">
            <p class="text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate distinctio perspiciatis odio aliquam! Eos dolorem voluptatem delectus alias at laudantium aspernatur impedit perspiciatis magnam explicabo adipisci, hic, repudiandae illo voluptatibus.
            Dolore, at consequatur vero facilis quibusdam magnam sunt nemo tempora autem iure deleniti eveniet ut nostrum aliquam voluptate laboriosam accusamus commodi sit amet molestias! Porro temporibus nam cupiditate obcaecati nisi.
            Natus modi ratione quisquam impedit iure, suscipit id repudiandae magni aut porro. Cumque, necessitatibus rem omnis veritatis odit nihil similique illo expedita ipsam error fugiat nam! Excepturi rem perferendis doloremque?
            Enim perspiciatis totam molestiae veritatis, asperiores officia placeat voluptatum non aliquam impedit et, magnam quod beatae vitae natus, aperiam rerum! Facilis molestias nulla quae inventore temporibus quam odio porro omnis.
            Itaque dolores, sequi ut tempore, magnam dolorum minima autem qui quo, distinctio perspiciatis! Cum sequi est quidem. Doloribus blanditiis nesciunt a! Ratione possimus minima, ducimus sapiente doloremque totam tempora harum?
            Tempora velit, ratione necessitatibus ipsa dignissimos numquam sequi illo blanditiis accusamus, autem maiores distinctio delectus odio adipisci laboriosam, sunt error! Cumque praesentium et maxime eius ad? Magni quia hic sapiente.</p>
        </section>
        <button @click="homePush">Powrót</button>
    </div>
</template>
<script>
import { useRouter } from "vue-router";
export default {
    data(){
        return{
             router: useRouter(),
        }
    },
    methods:{
        homePush(){
            this.router.push('/')
        }
    }
}
</script>
<style scoped>

.container{
    display: flex;
    align-items: flex-end;
    justify-content: center;
    border-radius: 50px;
    margin: 15px 15px;
    flex-direction: column;
    padding: 15px;
    box-shadow: 0 0 15px #ddd;
    border-radius: 5px;
}
section{
    display: flex;
}

img{
    width: 300px;
    height: 300px;
    border-radius: 5px;
}
.text{
    border-radius: 5px;
    padding-left: 15px;

}
button{
    /* border: 2px solid #999; */
    color: #aaa;
    border-radius: 15px;
    padding: 8px 15px;
    text-transform: uppercase;
    font-weight: 600;

}
button:hover{
    color: rgb(81,167,38);
    border-color: rgb(81,167,38);
}
@media (max-width: 720px){
    .inner-container{
    padding: 80px 50px;
    }
}
@media (max-width: 500px){
    .inner-container{
    padding: 50px 20px;
    }
}
</style>