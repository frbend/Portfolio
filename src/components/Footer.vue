<template>
    <main>
        <div class="foot_container">
                <h1 class="head1">Connect</h1>
            <div class="connect">
            <button class="cvButton"><a id="cv" href="./Frantisek_Bendik_CV.pdf" target="_blank">Get my CV</a></button>
                <a href="mailto:frantabendik@gmail..com"><img class="img1" src="../assets/imgs/email.png" alt=""></a>
                <a href="https://www.linkedin.com/in/frantisek-bendik-478a94172/" target="_blank"><img class="img2" src="../assets/imgs/linkedin2.png" alt=""></a>
                <a class="linkThree" href="https://github.com/frbend?tab=repositories" target="_blank"><img class="img3" src="../assets/imgs/github2.png" alt=""></a>
            </div><br>
            <div>
                    <p>©Portfolio 2022 | Designed and developed by me 
                    <a class="info"
                       @mouseenter="usedTools = true" 
                       @mouseleave="usedTools = false"
                       > info</a></p>
                <transition name="footer_tooltip">
                    <div class="tools"
                         v-show="usedTools"> 
                        <h1>Tools used</h1>
                        <div class="tool xd">
                            <div class="img">
                                <img src="../assets/imgs/Adobe_XD.png" />
                            </div>
                            <div class="content">
                                <h3>Adobe Xd </h3>
                                <span class="tag">Prototyping tool</span>
                            </div>
                        </div>
                        <div class="tool vue">
                            <div class="img">
                                <img src="../assets/imgs/vue.png" />
                            </div>
                            <div class="content">
                                <h3>Vue </h3>
                                <span class="tag">Frontend</span>
                            </div>
                        </div>
                        <div class="tool gsap">
                            <div class="img">
                                <img src="../assets/imgs/gsap-greensock.svg" />
                            </div>
                            <div class="content">
                                <h3>GSAP </h3>
                                <span class="tag">Animations</span>
                            </div>
                        </div>
                        <div class="tool aos">
                            <div class="img">
                                <img src="../assets/imgs/aos.png" />
                            </div>
                            <div class="content">
                                <h3>AOS </h3>
                                <span class="tag">Scroll Animations</span>
                            </div>
                        </div>
                    </div>
                </transition>
            </div>
        </div>
    </main>
</template>

<script>


export default {
    name: 'footer',
    components:{
    },
    data(){
        return {
            usedTools: false
        }
    },
    methods:{
        delay(){
            setTimeout(() =>{this.usedTools = false}, 2000)
        }
    }
}
</script>


<style>
    .foot_container{
        border-top: 1px solid #2A3250;
        height: 160px;
    }

    .tools{
        float: right;
        text-align: left;
        position: absolute;
        right: 25px;
        height: 400px;
        width: 250px;
        border: 1px solid rgb(175, 175, 175);
        margin: -480px 100px 0 0;
        z-index: 999;
        background-color: white;
        padding: 10px 10px 10px 30px;
        font-size: .7em;
    }
    .tools h3{
        margin-right: 25px;
        color: black;
    }
    .tools h1{
        text-align: center;
    }
    .tool{
        align-items: center;
        display: flex;
        margin-top: 1.5rem;
    }
    .img{
        width: 40px;
        height: 40px;
        background-color: rgba(0,0,0,.07);
        border-radius: 10rem;
        margin-right: 10px;
    }
    .img img{
        object-fit: contain;
        margin: 8px 0px 0px 8px;
        width: 25px;
        height: 25px;
    }
    .info{
        cursor: pointer;
        text-decoration: underline;
    }

    .connect{
        clear: both;
        position: relative;
    }

    .connect a{
        float: right;
    }
    .cvButton{
        text-transform: uppercase;
        background-color: #2A3250;
        color: white;
        width: 120px;
        height: 40px;
        border: none;
        border-radius: 13px;
        padding: 0 10px 0 10px;
        transform: translate(45%, 0%)
    }
    .cvButton a{
        margin: 0 12%;
    }
    .cvButton a:visited{
        color: white;
    }
    .cvButton a:link{
        color: white
    }
    .cvButton:hover{
        background-color: rgb(68, 100, 214);
        transition: 1s;
    }
    .head1{
        align-content: center;
    }
    img{
        width: 40px;
        height: 40px;
    }
    .img3{
        margin-top: 3px;
        width: 32px;
        height: 32px;
    }
    .connect a{
        text-decoration: none;
    }
    .footer_tooltip-enter-active,
    .footer_tooltip-leave-active{
        transition: opacity .8s ease
    }
    .footer_tooltip-enter-from,
    .footer_tooltip-leave-to{
        opacity: 0;   
    }


</style>