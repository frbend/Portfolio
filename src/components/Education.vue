<!--Comment section

-->


<template>
<main>
    <div class="placeholder_two">
        <div class="container">
            <h1 class="header" data-aos="fade-left" data-aos-duration="2000">Education</h1>
            <h4 class="diplomas" data-aos="fade-left" data-aos-duration="2400">Diplomas available per request</h4>
            <a href="https://www.baaa.dk/programmes/bachelor-s-top-up-degree/web-development/" target="_blank" >
                <div 
                    data-aos="fade-left" data-aos-duration="2000"
                    @mouseenter="showImageOne = true"
                    @mouseleave="showImageOne = false"
                    class="eaaa">
                    <p>Erhvervsakademi Aarhus</p>
                    <h3 class="wd">BA Top-Up Web Development (2019-2021)</h3>
                    <transition name="eaaa_image_one">
                        <img class="firstImage" v-show="showImageOne" src="../assets/imgs/eaaaimg.jpeg"/> 
                    </transition>
                </div>
            </a>
            <a href="https://www.easv.dk/da/uddannelser/multimediedesigner/" target="_blank">
                <div
                    data-aos="fade-left" data-aos-duration="2000"
                    @mouseenter="showImageTwo = true"
                    @mouseleave="showImageTwo = false"
                 class="easv">
                    <p>Erhvervsakademi Sydvest (Esbjerg)</p>
                    <h3 class="wd">AP Multimedia Design (2017-2019)</h3>
                    <transition name="easv_image_two">
                        <img class="secondImage" v-show="showImageTwo" src="../assets/imgs/easvimg.jpeg"/> 
                    </transition>
                </div>
            </a>
        </div>
    </div>
</main>

</template>

<script>



export default {
    name: 'aa',
    props:{
        text: String,
    },
    data(){
        return {
            showImageOne: false,
            showImageTwo: false,
        }
    },
    methods:{
        onClick(){
            console.log("this is working")
        },
        getImage(event){
            this.page.left = event.pageX;
            this.page.top = event.pageY;
            //console.log("X:" + event.clientX +" "+"Y:" + event.clientY + " " +this.showImage)
        },
        loadImage(){
            this.isLoaded = true
            console.log("img loaded")
        }
    }
}


//gsap.to(".diplomas", {duration: 2, scale: 0.5})

</script>


<style>
    .placeholder_two{
        margin-top: 15%;
        height: 600px;
    }
    .container .header{
        position: relative;
        font-weight: 600;
    }
    .container{
        float: left;
        margin-left: 20px;
    }
    .header{
        margin-left: 20px;
        font-size: 5em;
        width: 450px;
    }
    .diplomas{
        position: relative;
        float: left;
        bottom: 80px;
        margin-left: 25px;
        color: black;
    }
    .eaaa, .easv{
        position: relative;
        width: 800px;
        font-size: 2.5em;
        height: 200px;
        left: 50px;
        bottom: 70px;
        line-height: 70px;
    }
    .eaaa *, .easv *{
        margin: 0 0 0 25px;
        float: left;
        font-weight: 700;
    }
     .easv{
        top: 40px;
    } 
    .firstImage{
        /* No position else the image won't come back 
        position: absolute; */
        z-index: 1000;
        margin: -250px 0 0 650px;
        width: 500px; 
        height: 300px;
        overflow: hidden;
    }
    .secondImage{
        z-index: 1000;
        margin: -60px 0 0 650px;
        width: 500px;
        height: 300px;
        overflow: hidden;
    }
    .wd{
        font-size: 0.7em;
        color: black;
    }
    .eaaa_image_one-enter-active,
    .eaaa_image_one-leave-active{
        transition: opacity .8s ease
    }
    .eaaa_image_one-enter-from,
    .eaaa_image_one-leave-to{
        opacity: 0;   
    }
    .easv_image_two-enter-active,
    .easv_image_two-leave-active{
        transition: opacity .8s ease
    }
    .easv_image_two-enter-from,
    .easv_image_two-leave-to{
        opacity: 0;   
    }
</style>