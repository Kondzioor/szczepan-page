<template>
<div class="container">
        <div class="inner-container">
                <h1> O mnie
                    <div class="border"></div>
                </h1>
                <p class="text">
               Lorem*5
                </p>
                <button @click="homePush">Powrót</button>
        </div>
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
    height: 3px;
    width: 100px;
    background-color:rgb(86, 129, 64)  ;
}
.text
{
    font-size: 16px;
    color: #444;
    line-height: 30px;
    text-align: justify;
    margin-bottom: 40px;
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