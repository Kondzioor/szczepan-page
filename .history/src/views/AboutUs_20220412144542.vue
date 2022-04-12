<template>
<div class="container">
        <section>
            <img src="../assets/boy.jpg" alt="">
            <p class="text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla expedita suscipit minus rerum ea sed explicabo iusto eveniet esse nam! Ut asperiores nisi adipisci perspiciatis amet atque officia temporibus rem.
            Nostrum nemo repellat necessitatibus ullam perferendis vero eum deserunt mollitia nesciunt, fuga magnam aliquid quam quas cupiditate quia harum corporis hic? Debitis tempore illum sit repudiandae cumque consequuntur a necessitatibus.
            Aperiam tempora sit quam nostrum eius obcaecati voluptates ullam architecto asperiores officiis sint doloribus esse quia ex quibusdam animi delectus, in dignissimos vero quos natus voluptatibus cupiditate. Consequuntur, odit nostrum.
            Doloribus tempora necessitatibus sapiente odit quibusdam! Ratione labore dolore odio deserunt eligendi nihil enim accusamus quisquam optio, veniam perferendis sed magni esse nostrum atque officiis rem asperiores saepe reprehenderit consectetur?</p>
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
    align-items: center;
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
    border: 2px solid #999;
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