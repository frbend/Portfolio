<!--
-->


<template>
    <main>
        <div class="placeholder_three">
            <div class="container-two">
                <h1 class="work-exp" data-aos="fade-right" data-aos-duration="1500">Previous work</h1>
                <h1 class="freelance-heading" data-aos="fade-right" data-aos-duration="2000">Freelance</h1><br>
                <div class="freelance">
                    <div class="jap-translations"
                        data-aos="fade-right" data-aos-duration="2000">
                        <a
                            class="jap-translations-link" 
                            href="http://en.japonstina-tlumoceni.cz" 
                            target="_blank"
                            @mouseenter="showText1 = true"
                            @mouseleave="showText1 = false"
                            @mouseover="rotateArrow"
                            @mouseout="rotateArrowBack"
                            >Japanese Translations 
                        </a>
                        <a 
                            class="right-arrow"
                            href="http://en.japonstina-tlumoceni.cz" 
                            target="_blank"
                            @mouseover="rotateArrow"
                            @mouseleave="rotateArrowBack">&rarr;
                        </a><br>
                    </div>
                        <transition name="jap-translation-tooltip1">
                            <p v-show="showText1"
                            class="tooltip1">Freelancing paid project to create and maintain a WordPress website for an independent translator.</p> 
                        </transition>   
                    <div class="repair-exhibit"
                         data-aos="fade-right" data-aos-duration="2500">
                        <a 
                            class="repair-exhibit-link"
                            href="" 
                            @mouseenter="showText2 = true"
                            @mouseleave="showText2 = false"
                            @mouseover="rotateArrow2"
                            @mouseout="rotateArrow2Back"
                            >Repair Exhibit
                        </a>
                            <a 
                            class="right-arrow2"
                            href="" 
                            @mouseover="rotateArrow2"
                            @mouseleave="rotateArrow2Back">&rarr;
                        </a>
                    </div>
                        <transition name="repair-tooltip2">
                            <p v-show="showText2"
                            class="tooltip2">Short term paid project in collaboration with anthropology department of Aarhus University to create an online art exhibition due to covid shutdown.</p> 
                        </transition>   
                </div>
            </div>
                <div class="school">
                    <h1 data-aos="fade-left" data-aos-duration="1500"
                        >Bachelor's degree project
                    </h1>
                    <div class="voice-controlled-app"
                         data-aos="fade-left" data-aos-duration="2500">
                        <a 
                            class="desc"
                            href="https://frbend-voice-list.netlify.app/"
                            target="_blank"
                            @mouseenter="showText3 = true"
                            @mouseleave="showText3 = false"
                            @mouseover="rotateArrow3"
                            @mouseout="rotateArrow3Back"
                            >Voice controlled shopping list <br>Application (Javascript,html,css)
                        </a>
                        <a 
                            class="left-arrow"
                            href="https://frbend-voice-list.netlify.app/"
                            target="_blank"
                            @mouseover="rotateArrow3"
                            @mouseleave="rotateArrow3Back">&rarr;
                        </a>
                    </div>
                        <transition name="voice-control-tooltip3">
                                <p v-show="showText3"
                                class="tooltip3">Voice controlled shopping list application prototype. 
                                The goal was to show how Føtex plus app shopping list section could be optimised
                                by adding voice control option. Tasks included: find relevant technology,
                                build a prototype, contact Føtex department and present a solution, write a report</p> 
                        </transition> 
                    <!--
                        link to deployed project: https://frbend-voice-list.netlify.app/
                    -->
                </div>
                <div class="internship">
                    <h1 class="multimedia"
                        data-aos="fade-left" data-aos-duration="1500"
                        >Multimedia design internship
                    </h1>
                    <div class="kayor-group-internship"
                         data-aos="fade-left" data-aos-duration="2500">
                        <a 
                           class="desc"
                           href=""
                           @mouseenter="showText4 = true"
                           @mouseleave="showText4 = false"
                           @mouseover="rotateArrow4"
                           @mouseout="rotateArrow4Back"
                           >Kayor group
                        </a>
                        <a class="left-arrow2"
                            @mouseover="rotateArrow4"
                            @mouseleave="rotateArrow4Back">&rarr;
                        </a>
                    </div>
                        <transition name="kayor-group-tooltip4">
                            <p v-show="showText4"
                            class="tooltip4">Internship under a startup company. The tasks included:
                            design social media profile and cover pictures, design and rework of new logo,
                            development of new website with WordPress.</p> 
                      </transition> 

                </div>
                <div class="other-work">
                    <h1 data-aos="fade-right" data-aos-duration="1500">Other positions</h1>
                    <h1 data-aos="fade-right" data-aos-duration="1500">Student jobs</h1>
                    <div class="faust">
                        <h3 class="position" data-aos="fade-right" data-aos-duration="2000"
                        >Dishwasher</h3>
                        <h3 data-aos="fade-right" data-aos-duration="2000">Café Faust, Aarhus</h3>
                        <h3 data-aos="fade-right" data-aos-duration="2000">11/2019-03/2021</h3>
                    </div>
                    <div class="novasol">
                        <h3 class="position" data-aos="fade-right" data-aos-duration="2000"
                        >Cleaner of summer houses on Fanø island</h3>
                        <h3 data-aos="fade-right" data-aos-duration="2000">Novasol, Fanø, Esbjerg</h3>
                        <h3 data-aos="fade-right" data-aos-duration="2000">04/2019-08/2019</h3>
                    </div>
                        <div class="industrien">
                        <h3 class="position" data-aos="fade-right" data-aos-duration="2000"
                        >Cleaner of bar in Esbjerg center</h3>
                        <h3 data-aos="fade-right" data-aos-duration="2000">Industrien, Esbjerg</h3>
                        <h3 data-aos="fade-right" data-aos-duration="2000">03/2018-01/2019</h3>
                    </div>
                </div>
        </div>
    </main>
</template>

<script>
import gsap from "gsap";
export default {
    name: 'work',
    props:{
    },
    data(){
        return {
            showText1 : false,
            showText2 : false,
            showText3 : false,
            showText4 : false
        }
    },
    methods:{
        rotateArrow(){
            gsap.to(".right-arrow",{rotate:-25, duration: 0.1})
        },
        rotateArrowBack(){
            gsap.to(".right-arrow",{rotate: 0, duration: 0.1})
        },
        rotateArrow2(){
            gsap.to(".right-arrow2",{rotate:-25, duration: 0.1})
        },
        rotateArrow2Back(){
            gsap.to(".right-arrow2",{rotate: 0, duration: 0.2})
        },
        rotateArrow3(){
            gsap.to(".left-arrow",{rotate:-25, duration: 0.1})
        },
        rotateArrow3Back(){
            gsap.to(".left-arrow",{rotate: 0, duration: 0.2})
        },
        rotateArrow4(){
            gsap.to(".left-arrow2",{rotate:-25, duration: 0.1})
        },
        rotateArrow4Back(){
            gsap.to(".left-arrow2",{rotate: 0, duration: 0.2})
        }
    }
}
</script>



<style>
    .placeholder_three{
        height: 1500px;
    }
    .container-two{
        float: right;
        margin-right: 20px;
        margin-top: 10%;
        height: 500px;
    }
    .work-exp{
        font-size: 5em;
        width: 700px;
    }
    .freelance-heading{
        width: 220px;
        float: right;
        margin-right: 20px;
        font-size: 2.5em;
    }
    .freelance{
        position: relative;
        width: 400px;
        height: 200px;
        right: 50px;
        top: 100px;
        left: 200px;
    }
    .jap-translations-link, .repair-exhibit-link{
        font-size: 1.7em;
        font-weight: 700;
        line-height: 100px;
    }
    .tooltip {
        position: absolute!important;
        z-index: 1000;
        margin: 0px 0px 0px -1050px;
        width: 700px; 
        height: 500px;
        overflow: hidden;
    }   
    .freelance a{
        text-decoration: none;
        color: black;
    }
    .freelance a:hover, .freelance .right-arrow:hover, .freelance .right-arrow:hover,
    .left-arrow:hover, .left-arrow2:hover, .desc:hover, .aa:hover ~ .right-arrow,
    .repair-exhibit-link:hover ~ .right-arrow2, .desc:hover ~ .left-arrow, .desc:hover ~.left-arrow2{
        color: lightblue;
        transition: 0.3s;
    }
    .school, .internship{
        position: relative;
        clear: both;
        width: 700px;
        height: 200px;
        top: 70px;
        left: 20px;
        font-size: 1.5em;
        font-weight: 500;
    }
    .multimedia{
        width: 780px;
    }
    .desc{
        position: relative;
        left: 40px;
        color: black;
        float: left;
        text-decoration: none;
        text-align: left;
        font-weight: 700;
        font-size: 1em;
    }
    .other-work{
        position: relative;
        height: 500px;
        width: 480px;
        top: 100px;
        float: right;
        text-align: right;
        margin-right: 25px;
    }
    .faust, .novasol, .industrien{
        position: relative;
        right: 50px;
        margin-bottom: 30px;
        line-height: 10px;
        width: 500px;
    }
    .position{
        color: black;
    }
    .jap-translations, .repair-exhibit{
        width: 420px;
        height: 100px;
        text-align: left;
        position: relative;
    }
    .right-arrow, .right-arrow2, .left-arrow, .left-arrow2{
        font-size: 80px;
        height: 100px;
        position: absolute;
        margin: -2px 0px 0px 50px;
    }
    .right-arrow2{
        margin: -2px 0px 0px 180px;
    }
    .left-arrow{
        margin: -25px 0 0 0;
        text-decoration: none;
    }
    .left-arrow2{
        margin: -30px 0 0 130px;
    }
    .tooltip1{
        padding-top: 40px!important;
    }
    .tooltip1, .tooltip2, .tooltip3, .tooltip4{
        text-transform: none;
        padding: 30px;
        position: absolute;
        border: 1px solid #2A3250;
        border-radius: 50px;
        background-color: rgb(247, 247, 247);
        text-align: left;
        font-style: italic;
    }
    .tooltip1, .tooltip2{
        margin: -220px -90px 10px -400px;
        height: 80px;
        width: 300px;
    }
    .tooltip3, .tooltip4{
        margin: -30px 0px 0px 800px;
        height: 100px;
        width: 300px;
        padding-top: 40px !important;
        font-size: .6em;
    }
    .tooltip3{
        height: 150px;
        
    }
    .jap-translation-tooltip1-enter-active,
    .jap-translation-tooltip1-leave-active{
        transition: opacity .8s ease
    }
    .jap-translation-tooltip1-enter-from,
    .jap-translation-tooltip1-leave-to{
        opacity: 0;   
    }
    .repair-tooltip2-enter-active,
    .repair-tooltip2-leave-active{
        transition: opacity .8s ease
    }
    .repair-tooltip2-enter-from,
    .repair-tooltip2-leave-to{
        opacity: 0;   
    }
    .voice-control-tooltip3-enter-active,
    .voice-control-tooltip3-leave-active{
        transition: opacity .8s ease
    }
    .voice-control-tooltip3-enter-from,
    .voice-control-tooltip3-leave-to{
        opacity: 0;   
    }
    .kayor-group-tooltip4-enter-active,
    .kayor-group-tooltip4-leave-active{
        transition: opacity .8s ease
    }
    .kayor-group-tooltip4-enter-from,
    .kayor-group-tooltip4-leave-to{
        opacity: 0;   
    }
     @media only screen and (min-width: 320px) and (max-width: 600px) {
         .other-work{
             float: left;
             margin-left: 150vw;
         }
         .freelance-heading, .freelance, .jap-translations, .repair-exhibit, .container-two{
             float: left;
         }
         .freelance{
             margin-left: -400px;
         }
         .freelance-heading{
             margin-left: 25px;
         }
     }
         /*tablets*/ 
    @media only screen and (min-width: 760px) and (max-width: 768px){
        .other-work{
            margin-right: -300px;
        }
         .freelance-heading, .freelance{
             float: left;
             margin-left: 25px;
         }
         .jap-translations, .repair-exhibit{
              margin-left: -460px;
          }
    }
</style>