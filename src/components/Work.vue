<!--
- make iframe for japanese translations
- make animation on mousewheel? to make text appear as you scroll

-->


<template>
    <main>
        <div class="placeholder_three">
            <div class="containerr">
                <h1 class="work_exp" data-aos="fade-right" data-aos-duration="1500">Previous work</h1>
                <h1 class="free" data-aos="fade-right" data-aos-duration="2000">Freelance</h1><br>
                <div class="freelance">
                    <a @mouseover="firstIframe = true" 
                       @mouseleave="firstIframe = false" 
                       class="aa" 
                       href="http://en.japonstina-tlumoceni.cz" 
                       target="_blank"
                       data-aos="fade-right" data-aos-duration="2000"
                       >Japanese Translations
                        <iframe class="tooltip" 
                        v-show="firstIframe" 
                        ref="iframeOne" src="http://en.japonstina-tlumoceni.cz"
                        ></iframe>
                    </a><br>
                    <a class="aaa"
                       href="" 
                       data-aos="fade-right" data-aos-duration="2500">Repair Exhibit</a>
                </div><br>
            </div>
                <div class="school">
                    <h1 data-aos="fade-left" data-aos-duration="1500"
                    >Bachelor's degree project</h1>
                    <h3 class="desc"
                    data-aos="fade-left" data-aos-duration="2500"
                    >Voice controlled shopping list Application<br>(Javascript,html,css)</h3>
                    <!--
                        link to deployed project: https://frbend-voice-list.netlify.app/
                    -->
                </div>
                <div class="internship">
                    <h1 class="multi"
                    data-aos="fade-left" data-aos-duration="1500"
                    >Multimedia design internship</h1>
                    <h3 class="desc"
                    data-aos="fade-left" data-aos-duration="2500"
                    >Kayor group (put files on cloud and attach a link)</h3>
                </div>
                <div class="other_work">
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

export default {
    name: 'work',
    props:{
    },
    data(){
        return {
            firstIframe: false,
        }
    },
    methods:{
    }
}


</script>



<style>
    .placeholder_three{
        height: 800px;
    }
    .containerr{
        float: right;
        margin-right: 20px;
        margin-top: 10%;
        height: 500px;
    }
    .work_exp{
        font-size: 5em;
        width: 700px;
    }
    .free{
        width: 220px;
        float: right;
        margin-right: 20px;
        font-size: 2.5em;
    }
    .freelance{
        position: relative;
        width: 400px;
        height: 120px;
        right: 50px;
        top: 100px;
        left: 200px;
    }

    .aa, .aaa{
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
        float: right;
    }
    .freelance a:hover{
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
    .multi{
        width: 780px;
    }
    .desc{
        position: relative;
        width: 700px;
        left: 40px;
        color: black;
        text-align: left;
    }
    .other_work{
        position: relative;
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
    }
    .position{
        color: black;

    }

</style>