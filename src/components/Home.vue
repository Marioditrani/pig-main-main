<script>
export default{
    data(){
        return{
            obs:0,
            slides:[
            {image: "https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/70222220826_FedPig_B1_Traditional4_0401.jpg?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5",
             text:'lorem prima'},
            {image:"https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/67494IMG_2648.JPG?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.44&fp-y=0.66",
            text : 'lorem seconda'},
            {image:"https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/41145federalist-pig-home-pattern-black.jpg?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5",
            text : 'lorem terza'},
            {image:"https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/6865220826_FedPig_A3_FavTraditional_0110.jpg?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.48&fp-y=0.98",
            text : 'lorem seconda'},
            {image:"https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/95907IMG_6837.JPG?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5",
            text : 'lorem seconda'},
            ]
        };
    },
    methods: {
        primaImg(){
            this.obs = 0
        },
        secondaImg(){
             this.obs = 1
        },
        terzaImg(){
             this.obs = 2
        },
        quartaImg(){
             this.obs = 3
        },
        quintaImg(){
             this.obs = 4
        },
    }
}

</script>

<template>
    <div class="carousel">
        <div class="carousel-image" v-for="(slide, i) in slides" :key="slide">
                <div id="img-c" v-if="i == obs" v-bind:class="{'bg1': obs == 0,'bg2': obs == 1,'bg3': obs == 2,'bg4': obs == 3,'bg5': obs == 4,'bg6': obs == 5,}">
                    <p>{{ slide.text }}</p>
                    <div class="carousel-button">
                        <div class="button1" :class="obs == 0 ? 'btn-active' : ''" @click="primaImg"></div>
                        <div class="button2" :class="obs == 1 ? 'btn-active' : ''" @click="secondaImg"></div>
                        <div class="button3" :class="obs == 2 ? 'btn-active' : ''" @click="terzaImg"></div>
                        <div class="button4" :class="obs == 3 ? 'btn-active' : ''" @click="quartaImg"></div>
                        <div class="button5" :class="obs == 4 ? 'btn-active' : ''" @click="quintaImg"></div>
                    </div>
                </div>
        </div>
    </div>
    <div class="box1">
        <div class="img-card">
            <div class="card-left">
                <img src="https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/85291IMG_3966_web.jpg?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5" alt="">
                <h1>SPECIALS</h1>
                <p>Pitmaster Rob is always up to something! Check out our rotating specialty sandwiches and limited drops. Dino Beef Short Rib Combo for 2 is available every Monday & Tuesday.</p>
                <span>SEE ALL SPECIALS</span>
            </div>
            <div class="card-left">
                <img src="https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/98058IMG_1800.JPG?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5" alt="">
                <h1>SUPPER CLUB</h1>
                <p>Once a month, Chef & Pitmaster Rob Sonderman presents a new 4-course dine-in experience that goes beyond our regular offerings and puts a smoky spin on gourmet cuisine.</p>
                <span>GET YOUR TICKETS</span>
            </div>
            
        </div>
        
       
        
    </div>
    <div class="box2">
        <div class="box2-left">
            <div class="content">
            <h1>MENU</h1>
            <p>We’re craft American BBQ made in-house (always). Get traditions and favorites from all over the world — all on one plate. Federalist Pig is a two-time Michelin Bib Gourmand winner serving up DC’s best blend of the classic BBQ traditions you’d find at the most elite cookout and the elevated flavors you’d find at a true fine dining spot.
            Everything we serve is house-made and prepared by a staff that cares. You could spend a lifetime sampling every flavor combination at Federalist Pig, and we hope you do.</p>
            <span>PEEP THE MENU</span>
            </div>
        </div>
        <div class="box2-right">
            <img src="https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/58030220826_FedPig_A7_BCRcombo1_0264.jpg?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5" alt="">
        </div>
    </div>
    <div class="box3">
        <div class="box3-right">
            <img src="https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/86609220826_FedPig_B1_Traditional4_0411.jpg?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5" alt="">
        </div>
        <div class="box3-left">
            <div class="content">
            <h1>CATERING</h1>
            <p>We'll bring the 'que to you! From backyard bbq's, holiday celebrations or hundred-person events, our Barbecrew and catering truck can do it all. Serving thoughtfully crafted sides, vegan and vegetarian options, to the BBQ classics from all the regions of America, and all the corners of the globe — it’s all here.</p>
            <span> EXPLORE CATERING</span>
            </div>
        </div>
    </div>
    <div class="inf-bar">
        <div class="logos">
            <div class="logos-slide">
                <img src="https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/catalogue_brand_family-federalist-pig.png?w=1000&fit=max&auto=compress,format&h=1000" alt="">
            </div>
            <div class="logos-slide">
                <img src="https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/catalogue_brand_family-federalist-pig.png?w=1000&fit=max&auto=compress,format&h=1000" alt="">
            </div>
            <div class="logos-slide">
                <img src="https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/catalogue_brand_family-federalist-pig.png?w=1000&fit=max&auto=compress,format&h=1000" alt="">
            </div>
        </div>
    </div>
    <div class="footer">
        <div class="logo-contact">
            <div class="logo-fb">
                <i class="bi bi-facebook"></i>
            </div>
            <div class="logo-insta">
                <i class="bi bi-instagram"></i>
            </div>
        </div>
        <ul class="btn-footer">
            <li class="btn">AWARDS</li>
            <li class="btn">CAREERS</li>
            <li class="btn">CONTACT</li>
            <li class="btn">ABOUT</li>
            <li class="btn">TERMS</li>
            <li class="btn">PRIVACY</li>
            <li class="btn-large">EMAIL SIGNUP</li>
        </ul>
    </div>
<div class="footer-small">
    <span>ORDER NOW</span>
</div>
</template>

<style lang="scss" scoped>
.carousel{
    display: flex;
    flex-direction: column;
    align-items: center;
    .carousel-image{
        #img-c{
            height: 800px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
        }
        .carousel-button{
            gap: 13px;
            display: flex;
            background-color: #ffd700;
            padding: 17px;
            max-width: 350px;
            margin: 10px;
            align-items: center;
            justify-content: center;
            border-top-left-radius: 20px;
            border-top-right-radius: 20px;
            .button1, .button2, .button3, .button4, .button5{
            width: 13px;
            height: 13px;
            border-radius: 50%;
            background-color: black;
            opacity: .65;
            }
            .button1:hover, .button2:hover, .button3:hover, .button4:hover, .button5:hover{
                opacity: 1;
            }
            .btn-active{
                opacity: 1;
            }
        }
    }
}

.bg1{
    
    background-image: url("https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/70222220826_FedPig_B1_Traditional4_0401.jpg?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5");
}
.bg2{
    background-image: url("https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/67494IMG_2648.JPG?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.44&fp-y=0.66");

}
.bg3{
    background-image: url("https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/41145federalist-pig-home-pattern-black.jpg?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5");

}
.bg4{
    background-image: url("https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/6865220826_FedPig_A3_FavTraditional_0110.jpg?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.48&fp-y=0.98");

}
.bg5{
    background-image: url("https://images.getbento.com/accounts/22022076ca31682d32e6a3253b8e9e7c/media/images/95907IMG_6837.JPG?w=1200&fit=crop&auto=compress,format&crop=focalpoint&fp-x=0.5&fp-y=0.5");

}

.box1{
background-color: #ffd700;
padding: 60px 0px;

    .img-card{
        display: flex;
        gap: 40px;
        width: 60%;
        margin: auto;
            .card-left img, .card-right img{
                width: 100%;
                height: auto;
            }

        .card-left{
            display: flex;
            flex-direction: column;
            row-gap: 20px;
            text-align: center;
            justify-content: center;
            align-items: center;
            span{
                 border: 2px solid black;
                 padding: 5px 10px;
                 font-weight: bold;
                }
            span:hover{
                 padding: 5px 10px;
                 background-color: black;
                 color: #ffd700;
                 transition: all  linear 0.1s ;
            }
        }
    }   

@media (max-width: 980px) {
    .img-card{
    width: 90%;
    }
}


}
    

.box2{
    background-color: #ffd700;
    display: flex;
    padding-top: 40px;
    .box2-left{
        width: 40%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-self: center;
        
        
        .content{
            width: 80%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            row-gap: 40px;
            span{
                 border: 2px solid black;
                 padding: 5px 10px;
                 font-weight: bold;
                }
            span:hover{
                 padding: 5px 10px;
                 background-color: black;
                 color: #ffd700;
                 transition: all  linear 0.1s ;
            }
        }
    }
    .box2-right{
        width: 60%;
        height: auto;
        img{
            width: 100%;
            height: auto;
        }
    }
}
.box3{
    background-color: #ffd700;
    display: flex;
    
    .box3-left{
        width: 40%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-self: center;
        
        .content{
            width: 80%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            row-gap: 40px;
            span{
                 border: 2px solid black;
                 padding: 5px 10px;
                 font-weight: bold;
                }
            span:hover{
                 padding: 5px 10px;
                 background-color: black;
                 color: #ffd700;
                 transition: all  linear 0.1s ;
            }
        }
    }
    .box3-right{
        width: 60%;
        height: auto;
        img{
            width: 100%;
            height: auto;
        }
    }
}
.inf-bar{
    background-color: black;
    .logos{
        overflow: hidden;
        white-space: nowrap;
    }
    .logos-slide{
        animation: 30s slide infinite linear;
        display: inline-block;
    }
    
    @keyframes slide {
        from{
            transform: translateX(0);
        }
        to{
            transform: translateX(-100%);
        }
        
    }
}
.footer{
    background-color: black;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 40px;
    
    .logo-contact{
        height: 100%;
        display: flex;
        .logo-fb{
            width: 50px;
            height: 100%;
            border-radius: 50%;
            .bi ,.bi-facebook{
                font-size: 20px;
                color: #ffd700;
            }
        }
        .logo-insta{
            width: 50px;
            height: 100%;
            border-radius: 50%;
            .bi,.bi-instagram{
                font-size: 20px;
                color: #ffd700;
            } 
        }
    }
    .btn-footer{
        padding: 20px 0;
        text-align: center;
        align-items: center;
        display: flex;
        gap: 20px;
        .btn{
        color: #ffd700;
        
        }
        .btn-large{
        color: #ffd700;
        padding: 5px 10px;
        border: 2px solid #ffd700;
        }
    }
}
.footer-small {
    background-color: #ffd700;
    height: 100%;
    padding: 10px 0;
    text-align: center;
    font-size: 30px;
    display: none;
}
@media (max-width: 980px) {
    .footer-small{
        display: block;
    }
    .footer{
        display: none;
    }
}
@media (max-width: 768px) {
    .img-card, .box3 {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .box2 {
        padding-bottom: 20px;
        display: flex;
        flex-direction: column-reverse;
        align-items: center;

        .box2-left, .box2-right{
            width: 100%;
        }
    }


    .box3 {
        padding-bottom: 20px;
        .box3-right, .box3-left{
            width: 100%;
        }
    }

}
</style>