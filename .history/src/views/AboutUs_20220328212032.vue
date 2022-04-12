<template>
<div class="container">
        <div class="inner-container">
                <h1> O mnie
                    <div class="border"></div>
                </h1>
                <section>
                    <img src="../assets/boy.jpg" alt="">
                <p class="text">
               Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero a, id, accusantium rerum dignissimos, quia sint numquam nisi reiciendis inventore itaque quae laborum veniam eum voluptatum temporibus debitis qui labore.
               Minus non nulla aliquid hic quos porro rem architecto, incidunt voluptate doloribus, consequatur molestias qui dicta accusamus labore praesentium perferendis laborum commodi delectus eaque sit laudantium. Deserunt repudiandae ipsa quisquam.
               Consectetur assumenda porro excepturi quibusdam quidem veritatis quos natus eius a impedit cum, fugit voluptatibus animi at necessitatibus ea ipsam vel aperiam non fuga similique maiores modi expedita esse! Repudiandae.
               Nam eligendi dignissimos provident iste quas magnam enim maxime earum tenetur et consequatur eum architecto officia vel consectetur, deserunt odio quasi fugit neque doloremque illum molestias? Perferendis labore totam dicta.
               Accusamus blanditiis nam officiis iusto cumque eum ipsam iste id, voluptas obcaecati sapiente dolor reiciendis nesciunt amet nostrum deleniti. Dolorum amet neque itaque nisi adipisci accusantium rerum facere eligendi animi.
                </p>
                </section>

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
    height: 2px;
    width: 200px;
    background-color:#5b250a ;
}
.section{
    display: flex;
    flex-direction: row;
}
.img{
    max-width: 30%;
    max-height: 400px;
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