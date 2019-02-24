<template>
    <div>
        <h1>About <span>Me</span></h1>
        <div class="line"></div>
        <div class="content">
            <p><span>I am</span> a student at Telkom University, major in Diploma Degree in Computer Engineering and I am part of the robotic laboratory in my university. I have experience in electronic PCB design, Arduino, ROS, OpenCV, IOT, and many programming languages which are C++, Python, and JavaScript and also can do work with designing with Solidworks or Fusion360.</p>
            <p>Nowadays I'm at last year in my college and I'm doing a project on backend website development.</p>
            <!-- <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Blanditiis, repudiandae unde quia molestiae illum quae a accusamus dolore harum? Natus a sit beatae sequi quos tempora recusandae quam facere quae!</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Blanditiis, repudiandae unde quia molestiae illum quae a accusamus dolore harum? Natus a sit beatae sequi quos tempora recusandae quam facere quae!</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Blanditiis, repudiandae unde quia molestiae illum quae a accusamus dolore harum? Natus a sit beatae sequi quos tempora recusandae quam facere quae!</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Blanditiis, repudiandae unde quia molestiae illum quae a accusamus dolore harum? Natus a sit beatae sequi quos tempora recusandae quam facere quae!</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Blanditiis, repudiandae unde quia molestiae illum quae a accusamus dolore harum? Natus a sit beatae sequi quos tempora recusandae quam facere quae!</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Blanditiis, repudiandae unde quia molestiae illum quae a accusamus dolore harum? Natus a sit beatae sequi quos tempora recusandae quam facere quae!</p> -->
        </div>
        <div class="lineFooter">
            <h6>Copyright @ 2019</h6>
        </div>
    </div>    
</template>

<style lang="scss" scoped>
@import "../../assets/scss/config.scss";
h1, h6{
    text-align: center;

    span {
        color: $secondWordColor;
    }
}

.content {
    min-height: 58vh;
}

.line, .lineFooter {
    margin-top: 2vw;
    margin-bottom: 2vw;
    width: 92%;
    margin-left: 4%;
    margin-right: 4%;
    height: 5px;
    min-height: auto;
    background: $secondWordColor;
}

.lineFooter {
    h6 {
        margin: 0;
        padding: 1vw 0 1vw 0;
    }
}

p {
    margin: 0 0 3vw 0;
    padding-left: 3vw;
    padding-right: 3vw;
    font-size: 2.2vw;
    text-align: justify;

    span {
        color: $secondWordColor;
    }
}

//Smartphone Screen
@media screen and (max-width: 940px) {
    .content {
        min-height: 75vh;
    }

    .lineFooter {
        h6 {
            padding: 3vw 0 3vw 0;
        }
    }

    p {
        font-size: 4.5vw !important;
        padding: 2vw 6vw 0 6vw !important;
        text-align: justify !important;
    }
}

//Full HD Screen
@media screen and (min-width: 1920px) and (max-width: 2559px) {
    p {
        font-size: 1.8vw !important;
    }
}

//Bigger Screen
@media screen and (min-width: 2560px) {
    p {
        font-size: 1.5vw !important;
    }
}
</style>
