<template>
    <main>
        <div class="footer_container">
                <h1 class="head1">Connect</h1>
            <div class="connect">
                <button class="cv-button"><a id="cv" href="./Frantisek_Bendik_CV.pdf" target="_blank">Get my CV</a></button>
                <div class="social-links">
                    <a href="mailto:frantabendik@gmail..com"><img class="img1" src="../assets/imgs/email.png" alt=""></a>
                    <a href="https://www.linkedin.com/in/frantisek-bendik-478a94172/" target="_blank"><img class="img2" src="../assets/imgs/linkedin2.png" alt=""></a>
                    <a class="link-three" href="https://github.com/frbend?tab=repositories" target="_blank"><img class="img3" src="../assets/imgs/github2.png" alt=""></a>
                </div>
            </div><br>
            <div class="copyright-tools">
                    <p>©Portfolio 2022 | Designed and developed by me 
                    <a class="info"
                       @mouseenter="usedTools = true" 
                       @mouseleave="usedTools = false"
                       > info</a></p>
                <transition name="footer-tooltip">
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
    .footer_container{
        border-top: 1px solid #2A3250; 
        position: relative;
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
    .cv-button{
        text-transform: uppercase;
        background-color: #2A3250;
        color: white;
        width: 120px;
        height: 40px;
        border: none;
        border-radius: 13px;
        padding: 0 10px 0 10px;
    }
    .cv-button a{
        margin: 0 12%;
    }
    .cv-button a:visited{
        color: white;
    }
    .cv-button a:link{
        color: white
    }
    .cv-button:hover{
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
    .footer-tooltip-enter-active,
    .footer-tooltip-leave-active{
        transition: opacity .8s ease
    }
    .footer-tooltip-enter-from,
    .footer-tooltip-leave-to{
        opacity: 0;   
    }
    .social-links{
        transform: translate(0px, -40px);
    }
    .copyright-tools{
        width: 460px;
        margin-left: 410px;
    }

        /* Extra small devices (phones, 600px and down) */
    @media only screen and (min-width: 320px) and (max-width: 600px) {
        .footer_container{
            width: 1090px;
            height: 230px;
        }
        .copyright-tools{
            position: absolute; 
            top: 200px;
            right: 300px;
        }
        .social-links{
            position: absolute;
            transform: translate(490px, 30px);
        }
        .cv-button{
            width: 200px;
        }
        #cv{
            position: absolute;
            margin: -7px 50px 0px -35px;
            text-align: center;
        }

    }
        /*tablets and small laptops*/ 
    @media only screen and (min-width: 760px) and (max-width: 1024px){
        .footer_container{
            width: 1090px;
        }
        .social-links{
            position: absolute;
            transform: translate(950px, -40px);
        }
        .copyright-tools{
            position: absolute;
            right: 310px;
        }
    }
            /*4K screens*/ 
    @media only screen and (min-width: 2560px) and (max-width: 2600px){
        .copyright-tools{
            position: absolute;
            left: 630px;
        }
    }
</style>