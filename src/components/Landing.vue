<!--
 - need a box to animate and travel from side to side
 - on hover there could be transition covering only a piece
    and moving from left to right
- done
- if so move the third slider
-->


<template>
    <main>
        <div class="placeholder-one">
            <div class="areas">
                <div class="name-container" data-aos="fade-right" data-aos-duration="1500">
                    <h3 class="name">Frantisek Bendik</h3>
                </div><br>
                <div class="first-container" data-aos="fade-right" data-aos-duration="2000">
                    <h1 class="first">Web Developer</h1><br>
                </div>
                <!-- shinyEffect for cover1 also covers name section -->
                <div 
                    class="cover1"
                    @mouseover="shinyEffect"
                    @mouseleave="landingAnimationOut"
                ></div>
                <h1 class="second" data-aos="fade-right" data-aos-duration="2500">Graphic Designer</h1><br>
                <div 
                    class="cover2"
                    @mouseover="shinyEffect2"
                    @mouseleave="landingAnimationOutTwo"
                ></div>
                <h1 class="third" data-aos="fade-right" data-aos-duration="2900">Frontend Programmer</h1><br>
                <div 
                    class="cover3"
                    @mouseover="shinyEffect3"
                    @mouseleave="landingAnimationOutThree"
                ></div>
            </div>
                <div class="button-container">
                    <button class="buttonCV" data-aos="fade" data-aos-duration="1000"><a class="linkCV" href="#cv">Skip to CV</a></button>
                </div>
        </div>
    </main>
</template>


<script>
import gsap from "gsap";
//import {TimelineMax} from "gsap";
//TimelineMax
export default{
    name: 'landing',
    props:{},
    data(){
        return{}
    },
    methods:{
        shinyEffect(){
        gsap.to(".cover1", {duration: 2.5,ease:"circ.out" ,backgroundPositionX: -500});
        },
        landingAnimationOut(){
        gsap.to(".cover1", {backgroundPositionX: 500});
        },
        shinyEffect2(){
        gsap.to(".cover2", {duration: 2.5,ease:"circ.out" ,backgroundPositionX: -800});
        },
        landingAnimationOutTwo(){
        gsap.to(".cover2",{backgroundPositionX: 800})
        },
        shinyEffect3(){
        gsap.to(".cover3", {duration: 2.5,ease:"circ.out" ,backgroundPositionX: -800});
        },
        landingAnimationOutThree(){
        gsap.to(".cover3",{backgroundPositionX: 1000})
        },
    }
}
</script>

<style>
    .placeholder-one{
        margin-top: 10%;
        height: 500px;
    }
    .areas{
        position: relative;
        padding-top: 20px;
        width: 900px;
        height: 350px;
        font-size: 2em;
        margin: 30px 0 0 0px;
    }
    .areas h1{
        margin: 0;
    }
    .name-container{
        position: relative;
        float: left;
        margin-left: 20px;
        height: 60px;
        top: 40px;
    }
    .name{
        font-family: Oxygen, sans-serif;
        font-weight: 300;
        font-size: 20px;
    }
    .first{
        position: relative;
        top: 20px;
        float: left;
        font-weight: 400;
        z-index: 1;
    }
    .first-container{
        position: relative; 
        top: 20px;
        right: 19.5%;
        float: left;
        font-weight: 400;
    }
    .cover1{
        position: absolute;
        background-repeat:no-repeat;
        background-image: linear-gradient(to right, transparent, #ffffffea, transparent);
        background-position: -500px 0; 
        z-index: 9;
        width: 520px;
        height: 120px;
    }
    .cover2{
        position: absolute;
        background-repeat: no-repeat;
        background-image: linear-gradient(to right, transparent, #ffffffea, transparent);
        background-position: -700px 0;
        z-index: 9;
        width: 800px;
        height: 100px;
        margin: 75px 0px 0px 0px;
    }
    .cover3{
        position: absolute;
        background-repeat: no-repeat;
        background-image: linear-gradient(to right, transparent, #ffffffea, transparent);
        background-position: -800px 0;
        z-index: 9;
        width: 1000px;
        height: 100px;
        margin: -60px 0px 0px 50px;
    }
    .second{
        position: relative;
        float: left;
        top: 40px;
        left: 100px;
        font-weight: 400;
    }
    .third{
        position: relative;
        top: 50px;
        left: 200px;
        font-weight: 400;
    }
    .button-container{
        position: relative;
        left: 40vw;
        width: 200px;
        height: 150px;
        /* border: 1px solid black; */
    }
    .buttonCV{
        position: absolute;
        left: 40px;
        top: 60px;
        text-transform: uppercase;
        background-color: #2A3250;
        color: white;
        width: 120px;
        height: 40px;
        border: none;
        border-radius: 13px;
    }
    .buttonCV:hover{
        background-color: rgb(68, 100, 214);
        transition: 5s;
    }
    .linkCV{
        color: white!important;
        text-decoration: none;
    }
    /* Extra small devices (phones, 600px and down) */
    @media only screen and (min-width: 320px) and (max-width: 600px) {
        .buttonCV{
            left: 300px;
        }
        .other_work{
            width: 200px;
            height: 350px;
        }
    }
    /*tablets*/ 
    @media only screen and (min-width: 760px) and (max-width: 768px){
        .buttonCV{
            left: 150px;
        }
    }

</style>