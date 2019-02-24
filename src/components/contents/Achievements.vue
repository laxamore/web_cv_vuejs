<template>
    <div>
        <h1>Achieve<span>ments</span></h1>
        <div class="line"></div>
        <div class="content"></div>
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
}
</style>
 
