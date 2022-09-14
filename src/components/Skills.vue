<template>
    <main>
        <div class="placeholder_four">
            <div class="container-three">
                <h1 class="competencies"
                    data-aos="fade-left" data-aos-duration="1500"
                >Competencies</h1>
                <div class="frontend">
                    <h1 data-aos="fade-left" data-aos-duration="2000">Frontend technologies</h1>
                    <h3 data-aos="fade-left" data-aos-duration="2000">Javascript - Vanilla JS, Express JS</h3>
                    <h3 data-aos="fade-left" data-aos-duration="2000">frameworks - react, vue</h3>
                    <h3 data-aos="fade-left" data-aos-duration="2000">html5&css3, SCSS, pwa</h3>
                </div>
                <div class="design">
                    <h1 data-aos="fade-left" data-aos-duration="2000">Graphic design</h1>
                    <h3 data-aos="fade-left" data-aos-duration="2000">Adobe - Xd, Illustrator, Photoshop</h3>
                    <h3 data-aos="fade-left" data-aos-duration="2000">Figma</h3>
                </div>
                <div class="other">
                    <h1 data-aos="fade-left" data-aos-duration="2000">Other tools</h1>
                    <h3 data-aos="fade-left" data-aos-duration="2000">Wordpress</h3>
                    <h3 data-aos="fade-left" data-aos-duration="2000">Mongodb, Netlify</h3>
                    <h3 data-aos="fade-left" data-aos-duration="2000">Sql database management</h3>
                </div>
            </div>
        </div>
    </main>
</template>

<style>

    .placeholder_four{
        height: 800px;
        clear: both;
    }
    .competencies{
        font-size: 5em;
    }
    .container-three{
        position: relative;
        top: 100px;
        float: left;
        margin-left: 20px;
        text-align: left;
    }
    .frontend, .design, .other{
        position: relative;
        left: 50px;
        line-height: 20px;
        margin-bottom: 30px;
    }
    .frontend h3, .design h3, .other h3{
        color: black
    }

</style>