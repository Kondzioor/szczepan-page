<template>
<div class="container">
        <img src="../assets/boy.jpg" alt="">
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