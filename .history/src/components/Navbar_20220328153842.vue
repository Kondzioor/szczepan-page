<template>
    <div class="header">
        <nav>
            <div class="branding">
                <!-- <img class="logo" src="@/assets/images/logo.png" alt=""> -->
            </div>
            <ul v-if="!mobile" class="navigation">
                <li ><a class="link" href="#">Strona główna</a></li>
                <li ><a class="link" href="#">Galeria</a></li>
                <li ><a class="link" href="#">Kontakt</a></li>
                <li ><a class="link" href="#">Cennik</a></li>
            </ul>

            <div class="icon">
                <i @click="toggleMobileNav" v-show="mobile" class="fas fa-bars" :class="{'icon-active': mobileNav}"></i>
            </div>
            <transition name="mobile-nav">
                <ul v-if="mobileNav" class="dropdown-nav">
                    <li><a class="link" href="#" @click="productPush">Produkty</a></li>
                    <li v-if="isAdmin"><a class="link"  href="#" @click="newProductPush">Utwórz produkt</a></li>
                    <li v-if="isAdmin"><a class="link"  href="#" @click="categoriesPush">Kategorie</a></li>
                    <li v-if="isLoggedIn"><a class="link"  href="#" @click="historyPush">Historia</a></li>
                    <li v-if="!isLoggedIn"><a class="link"  href="#" @click="loginPush">Zaloguj</a></li>
                    <li v-if="!isLoggedIn"><a class="link"  href="#" @click="registerPush">Zarejestruj</a></li>
                    <li v-if="isLoggedIn"><a class="link"  href="#" @click="logout">Wyloguj</a></li>
                    <li v-if="!isAdmin && !isEmployee">

                    </li>
                </ul>
            </transition>
        </nav>
    </div>
</template>
<script>
import { useRouter } from "vue-router";
export default {

    data(){
        return{
            router: useRouter(),
            mobile: null,
            mobileNav: null,
            windowWidth: null,
        }
    },
    computed:{
    isLoggedIn(){
      return this.$store.getters.isAuth
    },
    isAdmin(){
      return this.$store.getters.isAdmin
    },
    getCartLength(){
      return this.$store.getters.getCart.length
    },
    isEmployee(){
        return this.$store.getters.isEmployee
    },

  },
  methods:{
    toggleMobileNav(){
        this.mobileNav = !this.mobileNav
    },

    checkScreen(){
        this.windowWidth = window.innerWidth;
        if(this.windowWidth <= 920){
            this.mobile = true
            return
        }
        this.mobile = false;
        this.mobileNav = false;
        return
    },
    homePush() {
        this.router.push('/');
      },
    productPush(){
        if(!this.isEmployee){
      this.router.push('/products')
        }
    },
    cartPush(){
        if(!this.$store.getters.isAuth){
            alert("Zaloguj aby przejść do koszyka")
        }else{
            this.router.push('/cart')
        }
    },
    loginPush(){
      this.router.push('/login')
    },
    registerPush(){
      this.router.push('/register')
    },
    logout(){
      this.$store.dispatch('logoutAction')
      this.router.push('/login')
    },
    historyPush(){
      this.router.push('/history')
    },
    categoriesPush(){
      this.router.push('/categories')
    },
    newProductPush(){
      this.router.push('/new_product')
    }
  },
  created(){
      window.addEventListener('resize',this.checkScreen);
      this.checkScreen();
  },
  mounted(){
    this.$store.dispatch('getUser')
    if(this.$store.getters.isAuth){
    this.$store.commit('setCart')
    this.$store.commit('setTotal')
    this.$store.commit('setHistory')
    }
  }
}
</script>
<style scoped>
.cart-icon{
    position: relative;
    margin-right: 20px;
    cursor:pointer;
}
.cart-icon span{
    background-color:rgb(81,167,38) ;
    border-radius: 20px;
    color: white;
    position: absolute;
    top:-11px;
    right: 0;
    padding: 5px 7px;
    font-size: 10px;
}

.header{
    max-width:  1230px;
    background-color: white;
    width: 100%;
    border-bottom: 1px solid #ddd;
    position: relative;
    transition: 0.5s ease all;
    color: green;
}
.logo{
    cursor: pointer;
}
nav{
    display: flex;
    flex-direction: row;
    padding: 12px 0;
    transition: .5s ease all;
    width:90%;
    margin: 0 auto;
    align-items: center;

}
ul,
.link {
    font-weight: 500;
    color: green;
    list-style: none;
    text-decoration: none;
}
li{
    text-transform: uppercase;
    padding: 16px;
    margin-left: 16px;
}
.link{
    font-size: 14px;
    transition: .5s ease all;
    padding-bottom: 4px;
    border-bottom: 1px solid transparent;
}
.link:hover{
    color: rgb(81,167,38);
    border-color: rgb(81,167,38);

}
.branding{

    display: flex;
    align-items: center;

}
.branding img{
    width:100%;
    transition: .5s ease all;
}
.navigation{
    display:flex;
    align-items: center;
    flex:1;
    justify-content: flex-end;
}
.icon{
    display: flex;
    align-items: center;
    position: absolute;
    top:0;
    right: 24px;
    height: 100%;
    z-index: 100;
}
i{
    cursor: pointer;
    font-size: 24px;
    transition: .8s ease all;
    margin-right: 40px;
}
.icon-active{
    transform: rotate(180deg);
}
.dropdown-nav{
    display: flex;
    flex-direction: column;
    position: fixed;
    width: 100%;
    max-width: 250px;
    height: 100%;
    background-color: #fff;
    top: 0;
    left: 0;
    z-index: 99;
}
.dropdown-nav li{
    margin-left: 0;

}
.mobile-nav-enter-active,
.mobile-nav-leave-active{
    transition: 1s ease all;
}
.mobile-nav-enter-from,
.mobile-nav-leave-to{
    transform: translateX(-250px)
}
.mobile-nav-enter-to{
    transform: translateX(0)
}
@media (max-width: 500px){
  .branding img{
      width: 230px;
  }
}
@media (max-width: 420px){
  i{
      margin-right: 10px;
  }
}
@media (max-width: 500px){
  .branding img{
      width: 180px;
  }
  i{
      margin-right: 5px;
  }
}
</style>