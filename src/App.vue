<template>
     
<header>
  <img src="./images/logo.svg" alt="Logo">
  <nav class="desktop">
    <a>PRODUCT</a>
    <a>FEATURES</a>
    <a>PRICING</a>
    <a class="nav-divider">&#8226;</a>
    <a class="nav-login">LOGIN</a>
  </nav>
  <button v-on:click="open" v-bind:class="{'mobile close': mobileMenu, 'mobile open': !mobileMenu}"></button>
  <div v-bind:class="{'mobile-menu open': mobileMenu, 'mobile-menu close': !mobileMenu}" style>
    <a>PRODUCT</a>
    <a>FEATURES</a>
    <a>PRICING</a>
    <a class="nav-login">LOGIN</a>
  </div>
</header>
<div class="content">
    <p><span>NEW</span>MONOGRAPH DASHBOARD</p>
    <h1>POWERFUL INSIGHTS <span>INTO YOUR TEAM</span></h1>
    <h2>Project planning and time tracking <span>for agile teams</span></h2>
    <div class="button-container">
      <button id="btnSchedule">SCHEDULE A DEMO</button>
      <label>TO SEE A PREVIEW</label>
    </div>
</div>
<div class="hero">

</div>
</template>

<script>

export default {
  data(){
    return {
        mobileMenu: false
    }
  },
  name: 'App',
  methods:{
    open(){
      this.mobileMenu = !this.mobileMenu;
    }
  }
}
</script>

<style >
@import url('https://fonts.googleapis.com/css2?family=Barlow&family=Barlow+Condensed:wght@400;700&display=swap');

:root{
  --Red: hsl(0, 100%, 68%);
  --VeryDarkBlue: hsl(230, 29%, 20%);
  --DarkGrayishBlue: hsl(230, 11%, 40%);
  --GrayishBlue:hsl(231, 7%, 65%);
  --LightGrayishBlue: hsl(207, 33%, 95%);
}
*{
  box-sizing: border-box;
  margin :0;
  padding: 0
}
html{
  overflow:auto; 
}
body{
  position:relative;
  overflow: hidden;

}

.mobile-menu{
  position: absolute;
  width: 80%;
  height: 0px;
  background-color: white;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  box-shadow: grey 0px .3rem .5rem;
  top: 100px;
  transition: all .2s ease;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: center;

  padding: 0rem;

  font-family: "Barlow Condensed";
  font-weight: 700;
  color: hsl(230, 29%, 20%);
  font-size: 1.25rem;
}

.mobile-menu > a {
  text-align: center;
  padding-top: 1rem;
  margin-bottom: 1rem;
}

.mobile-menu > a:last-child {
  
  border-top: 1px solid hsl(230, 11%, 40%);
}

.mobile-menu.open{
  padding: 2rem;
  height: 250px;
  max-height: 250px;
}

header{
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
}

  header > nav{
    font-family: "Barlow Condensed";
    font-weight: 700;
    font-size: 18px;
    display: flex;
    gap: 42px;
  }

    header > nav > a {
       color: var(--VeryDarkBlue);
       cursor: pointer;
       transition: border-bottom .2s ease;
    }

    header > nav > a:hover{
      border-bottom: 1px solid hsl(230, 29%, 20%);
    }

    header > nav > .nav-divider{
      cursor: auto;
      color: var(--GrayishBlue);
    }

    header > nav > a.nav-login{
      color: var(--DarkGrayishBlue);
      transition: border-bottom .2s ease;
    }

    header > nav > a.nav-login:hover{
      border-bottom: 1px solid var(--DarkGrayishBlue);
    }
.hero{
  content: url('./images/illustration-devices.svg');
}

img, svg{
  max-width: 100%;
  height: auto;
}

.bluecorner{
  background-color: rgb(237, 242, 246);
  position: absolute;
  border-radius: 0 0 0 4rem;
  height: 428px;
  width: 705px;
  top: 0;
  z-index: 1;
}

#app {
  position: relative;
  z-index: 2;
  /* background: no-repeat url('./images/illustration-devices.svg') top -13.813 right -16.7rem; */
  height: 100vh;
  width: 100vw;
  display: grid;
  
}

.content{
  display: flex;
  flex-direction: column;
  gap: 35px;
}

.content > p{
  font-family: "Barlow Condensed";
  letter-spacing: .2rem;
  color: hsl(231, 7%, 65%);
}

.content > p > span{
  background-color: hsl(230, 29%, 20%);
  color: hsl(207, 33%, 95%);
  letter-spacing: normal;
  margin-right: 10px;
  padding: 5px 10px;
  font-weight: 700;
  border-radius: 1rem;
}

h1{
  font-family: "Barlow Condensed";
  font-weight: 700;
  font-size: 3.5rem;
  color: hsl(230, 29%, 20%);
  display: flex;
  flex-direction: column;
}

h2{
  font-family: "Barlow";
  color: hsl(230, 11%, 40%);
  font-weight: 400;
  font-size: 1.25em;
  display: flex;
  flex-direction: column;
}

.button-container{
  display: flex;
  justify-content: start;
  align-items:center;
  gap: 1rem;
}
#btnSchedule{
  border: none;
  background-color: hsl(0, 100%, 68%);
  color:white;
  font-family: "Barlow Condensed";
  font-weight: 700;
  width: 190px;
  height: 50px;
  font-size: 1.125em;
  border-radius: 5px;
  padding: .5rem 0px;
  transition: background-color .2s ease;
  cursor: pointer;
}

#btnSchedule:hover{
  background-color: rgb(255, 133, 132);
}

.button-container > label{
  color: hsl(231, 7%, 65%);
  letter-spacing: .2rem;
  font-family: "Barlow Condensed";
}

button.mobile{
  width: 38px;
  height: 30px;
  transition: all .2s ease;
  background-repeat: no-repeat;
  background-position: center center;
  border: none;
  background-color: transparent;
}

button.mobile.open{
  transform: rotate(0deg);
  background-image: url('./images/icon-hamburger.svg');

}

button.mobile.close{
  transform: rotate(-90deg);
  background-image: url('./images/icon-close.svg');

}

@media screen and (min-width: 800px) {

  .mobile{
    display: none;
  }

  .desktop{
    display: flex;
  }
  .bluecorner{
      right:0;
  }

  #app{

    grid-template-rows: auto 1fr;
    grid-template-columns: 1fr 1fr;
  }

  header{
    padding: 0px 163px;
    height: 220px;
    grid-row: 1/2;
    grid-column: 1/3;

  }

  .hero{
    overflow: hidden;
    transform: translateX(1.5rem) translateY(-.5rem);

  }

  .content{
    gap: 1rem;
    padding: 40px 83px 0px 165px;
  }

  .content > h2 {
    margin-bottom: 35px;
  }
}

@media screen and (min-width: 280px) and (max-width: 799px){

  .mobile{
    display: block;
  }

  .desktop{
    display: none;
  }

  .bluecorner{
      right: auto;
      left: 50%;
  }

  header{
    padding: 0px 33px;
    height: 127px;
  }
  
  #app{
    height: auto;
    grid-template-columns: 1fr;
    grid-template-rows: auto auto 1fr;
  }

  .hero{
    width: 138%;

    grid-column: 1/2;
    grid-row: 2/3;

  }

  .content{
    gap: 32px;
    padding: 90px 33px 33px 33px;
    justify-content: center;
  }

  h1{
    font-size: 2.5rem;
  }

  #btnSchedule{
    width: 150px;
    font-size: .9rem;
    height: 40px;
  }

  .button-container > label{
    font-size: .9rem;
  }

}
</style>
