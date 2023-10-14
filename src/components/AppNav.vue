<script>
export default {
  data() {
     return {
       generalmenu: 0,
     }
    },
    methods: {
        menuside() {
        if (this.generalmenu) {
            this.generalmenu = 0
        } else {
            this.generalmenu = 1
        }
        console.log(this.generalmenu)
        },
    }
}
</script>

<template>
    <div class="header">
        <div class="logo">
            <span class="logo-up">federalist</span>
            <span class="logo-down">pig</span>
        </div>
        <ul class="nav">
            <li class="menu"> <span>menu</span></li>
            <li class="menu"><span>catering</span></li>
            <li class="menu"><span>locations</span></li>
            <li class="menu"><span>bbq box</span></li>
            <li class="menu"><span>supper club</span></li>
            <li class="menu"><span>gift cards</span></li>
            <li class="orders-online">orders online</li>
        </ul>
        <div class="icon-menu" @click=" menuside(generalmenu)" :class="generalmenu ? 'menuopen' : 'menuclose'">
            <div class="top-bar"></div>
            <div class="bottom-bar"></div>
        </div>
        <div class="menusideopen" :class="generalmenu ? 'menusideopen' : 'menusideclose'">
            <ul>
            <span class="menu">MENUS</span>
            <span class="menu">CATERING</span>
            <span class="menu">LOCATIONS</span>
            <span class="menu">BBQ BOX</span>
            <span class="menu">SUPPER CLUB</span>
            <span class="menu">GIFT CARDS</span>
            <span class="menu">AWARDS</span>
            <span class="menu">CAREERS</span>
            <span class="menu">CONTACT</span>
            <span class="menu">ABOUT</span>
            <span class="menu">TERMS</span>
            <span class="menu">PRIVACY</span>
            <span class="menu">ORDER ONLINE</span>
            <span class="menu">EMAIL SIGNUP</span>
        </ul>
        <div class="bar"></div>
        
        </div>
    </div>
</template>

<style lang="scss" scoped>
*{
    text-transform: uppercase;
    font-weight: bold;
}
.header{
    background-color: #ffd700;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    position: fixed;
    width: 100%;

    .icon-menu{
        width: 40px;
        height: 50px;
        display: none;
        margin-right: 20px;

        .top-bar{
            margin-top: 10px;
            height: 5px;
            width: 100%;
            background-color: black;
  
        }
        .bottom-bar{
            height: 6px;
            width: 100%;
            background-color: black;
            margin-top: 10px;
        }
    }
    .menuopen{
        z-index: 1;
    }
    .menusideopen {
    background-color: #ffd700;
    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0;
    right: 0;
    display: flex;
    transition: all  linear 0.2s ; 
    justify-content: center;
    flex-direction: column;
    align-items: center;
    ul{
        padding-top: 50px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        row-gap: 20px;
    }
    .bar{
        width: 90%;
        height: 3px;
        background-color: black;
        margin: 20px;
    }

}
.menusideclose {
  transition: all  linear 0.2s ;
  height: 0;
  ul{
    display: none;
  }
  
}
}
.logo{
   display: flex;
   flex-direction: column;
   font-size: 45px;
   padding: 5px 30px;
   
}

.nav{
    padding: 0px 30px;
    height: 100%;
    display: flex;
    gap: 20px;
    font-size: 16px;
    
}

.menu{
    padding: 7px 5px;
    position: relative;
    display: flex;
    align-items: center;
}
.orders-online{
    display: flex;
    align-items: center;
    justify-content: center;
}

.menu::after  {
    content: ' ';
    background-color: black;
    width: 0%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    transition: all linear 0.2s;
    z-index: 1;
    display: block;
}
.menu:hover::after{
    content: ' ';
    background-color: black;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    transition: all 0.2s linear  ;
    z-index: 1;
    display: block;
} 

.nav{
    .menu{
        span{
            color: black;
            padding: 0px 5px;
            transition: all 0.2s linear  0.2s;
            display: block;
            position: relative;
            z-index: 3;
        }
        span:hover{
            color: #ffd700;
            padding: 0px 5px;
            display: block;
            position: relative;
            z-index: 3;
            color: #ffd700;
            transition: all  linear 0.1s ;
        }
    }
}
.orders-online{
    border: 2px solid black;
    padding: 5px 5px;
}
.orders-online:hover{
    padding: 5px 5px;
    background-color: black;
    color: #ffd700;
    transition: all  linear 0.1s ;
}

@media (max-width: 1550px) {
  .header {
    display: flex;
    flex-direction: column;
    row-gap: 10px;
    padding-bottom: 40px;
  }
}
@media (max-width: 990px) {
  .header {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding-bottom: 0px;
    .nav{
        display: none;
    }
    .icon-menu{
        display: block;
    }
  }
}
</style>