<template>
<div class="container">
        <div class="inner-container">
                <h1>
                 O nas
                    <div class="border"></div>
                </h1>
                <p class="text">
                 Początek pasji jaką jest ziołolecznictwo miał miejsce podczas survivalowych wycieczek, które niejednokrotnie wiązały się z długimi pieszymi wędrówkami i nocami pod chmurką. <br>
                 To właśnie obcowanie z naturą uświadomiło nam, że najlepiej czujemy się w jej objęciach. Więc zaczęliśmy zdobywać wiedzę o tym czym darzy nas przyroda. Niejednokrotnie wyjazd do lasu czy na ryby, zamieniał się w poszukiwanie informacji na temat napotkanych roślin czy grzybów. I tak dowiadywaliśmy się, jakie mają działanie, komu są wskazane a dla kogo niepożądane, kiedy i jak zbierać i w końcu co robić z pozyskanych surowców.<br>
	Kolejne doświadczenia zdobywaliśmy robiąc samodzielnie maceraty, nalewki, syropy itp.,
następnie testując ich działania na sobie i członkach rodziny.<br>
	Te doświadczenia i wykształcenie jakie nabyliśmy pozwoliło nam na następny krok:<br>
- Otwarcie sklepu stacjonarnego, miejsca w którym oprócz gamy wyselekcjonowanych produktów możecie liczyć na porady i wsparcie.<br><br><br><br>
<span>Serdecznie zapraszamy!</span>
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
    padding: 100px 50px;
    border: 1px solid #ddd;
    border-radius: 50px;
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