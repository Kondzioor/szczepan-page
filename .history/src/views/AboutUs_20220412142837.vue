<template>
<div class="container">

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
            this.router.push('/products')
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
.inner-container{
    padding: 0 10px;
}
.inner-container h1{
    margin-bottom: 30px;
    font-size: 30px;
    font-weight: 800;
}
.border{
    height: 2px;
    width: 200px;
    background-color:#5b250a ;
}
section{
    display: flex;
}
.photo{
    background-color: black;
    width: 100px;
    height: 100px;
    /* flex-grow: 1;
    width: 500px;
    height: 500px;
    background-position-x: 65%;
    background-repeat: no-repeat;
    background-size: cover;
    background-image: url('../assets/boy.jpg'); */
}
.text
{
    /* font-size: 16px;
    color: #444;
    line-height: 30px;
    text-align: justify;
    margin-bottom: 40px; */
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
span{
    font-weight: bold;
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