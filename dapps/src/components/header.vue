<template>
  <div class="header-main">

    <div class="header-inner">
      
      <div class="header-button"><router-link to="/"><button>WALLETS</button></router-link></div>
      
      <div class="header-nav">
        <ul v-show="!mobile">
          <router-link to="/"> <li>HOME</li></router-link>
        <router-link to="/wallets">  <li class="li-int">INTEGRATE WALLETS</li></router-link>
       <router-link to="/">  <li>CONTACT</li></router-link>
        </ul>

        <div class="icon">
          <i @click="toggleMobilNav" v-show="mobile" class="fas fa-bars" :class="{'icon-active' : mobileNav}"></i>
        </div>

        <transition name="mobile-nav">
          <ul v-show="mobileNav" class="dropdown-nav">
          <router-link to="/"> <li>HOME</li></router-link>
        <router-link to="/wallets">  <li class="li-int">INTEGRATE WALLETS</li></router-link>
       <router-link to="/">  <li>CONTACT</li></router-link>
        </ul>
        </transition>
      </div>
    </div>
      
  </div>
</template>

<script>
export default {
  name: "navigation",
  data(){
    return{
      mobile: null,
      mobileNav:null,
      windowWidth:null,
    }
  },

  created(){
    window.addEventListener('resize', this.checkScreen);
    this.checkScreen();
  },

  methods:{
    toggleMobilNav(){
      this.mobileNav = !this.mobileNav;
    },

  checkScreen(){
    this.windowWidth = window.innerWidth;
    if(this.windowWidth <= 900){
      this.mobile = true;
      return;
    }
    this.mobile = false;
    this.mobileNav = false;
    return;
  }

  }

}
</script>

<style>

.icon{
  display: flex;
  position: absolute;
  align-items: center;
  top: 0;
  left:6rem ;
  height: 100%;
}
.icon i{
  cursor: pointer;
  font-size: 24px;
  transition: .8s ease all;
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
  height: 40%;
  top: 0;
  left: 0;
  background-color: white;
}
</style>