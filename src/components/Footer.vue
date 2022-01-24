<template>
    <main>
        <div class="foot_container">
            <div class="tools">
                <h1>Tools used</h1>
                <h3>Adobe Xd</h3>
                <h3>Vue</h3>
                <h3>GSAP (not yet tho)</h3>
            </div>
                <h1 class="head1">Connect</h1>
            <div class="connect">
            <button class="cvButton"><a id="cv" href="./Frantisek_Bendik_CV.pdf" target="_blank">Get my CV</a></button>
                <a href="mailto:frantabendik@gmail..com"><img class="img1" src="../assets/imgs/email.png" alt=""></a>
                <a href="https://www.linkedin.com/in/frantisek-bendik-478a94172/" target="_blank"><img class="img2" src="../assets/imgs/linkedin2.png" alt=""></a>
                <a class="linkThree" href="https://github.com/frbend?tab=repositories" target="_blank"><img class="img3" src="../assets/imgs/github2.png" alt=""></a>
            </div><br>
            <div>
                <p>©Portfolio 2022 | Designed and developed by me <a href=""> info</a></p>
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
        }
    },
    methods:{
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
        text-align: right;
        position: relative;
        right: 25px;
        display: none;
    }
    .tools h3{
        margin-right: 25px;
        color: black;
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



</style>