<template>
    <section class="hidden-sm-and-down">
        <div id="scroll-position" class="scroll-position">
            <div class="scroll-frame">
                <div @click="goHeader()" class="dot-scroll" />
                <div @click="goContent()" class="dot-scroll" />
                <div @click="goFooter()" class="dot-scroll" />
            </div>
        </div>
    </section>
</template>

<script>
import $ from "jquery";

export default {
    mounted() {
        // var defualtScroll = 0
        // var $w = $(window).scroll( function(event) {
            // var headerFrame = $('#header-frame').offset().top
            // var contentFrame = $('#content-frame').offset().top
            // var footerFrame = $('#footer-frame').offset().top
            // var checkScroll = $(this).scrollTop()

            // if(checkScroll > defualtScroll){
            //     if($w.scrollTop() > headerFrame && $w.scrollTop() < footerFrame){
            //         $('html, body').animate({
            //             scrollTop: $("#content-frame").offset().top
            //         }, 500);
            //         console.log('header layout')
            //     }
            //     else if($w.scrollTop() < contentFrame) {
            //         $('html, body').animate({
            //             scrollTop: $("#footer-frame").offset().top
            //         }, 500);
            //         console.log('content layout')
            //     }
            //     else {
            //         console.log('footer layout')
            //     }
            // }
            // else {
            //     if(checkScroll < contentFrame) {
            //         $('html, body').animate({
            //             scrollTop: $("#header-frame").offset().top
            //         }, 500);
            //     }
            // }

            // defualtScroll = checkScroll

            // console.log(headerFrame)
            // console.log(contentFrame)
            // console.log(footerFrame)

            // if($w.scrollTop() > 0){
            //     $(".scroll-position")
            //     .css({
            //         "display": "flex",
            //         "justify-content": "flex-end",
            //         "align-items": "center"
            //     });
            // }
            // else {
            //     $(".scroll-position")
            //     .css({
            //         "display": "none"
            //     });
            // }
        // });
    },
    methods: {
        goHeader() {
            $('html, body').animate({
                scrollTop: $("#header-frame").offset().top
            }, 500);
        },
        goContent() {
            $('html, body').animate({
                scrollTop: $("#content-frame").offset().top
            }, 500);
        },
        goFooter() {
            $('html, body').animate({
                scrollTop: $("#footer-frame").offset().top
            }, 500);
        }
    }
}
</script>

<style scoped>

.scroll-position {
    position: fixed;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    height: 100vh;
    right: 6rem;
}

.scroll-frame{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    height: 20rem;
    width: 0.2rem;
    background-color: black;
    border-radius: 1rem;
}

.dot-scroll {
    width: 2rem;
    height: 2rem;
    background-color: rgba(255,255,255,1);
    border-radius: 1rem;
    cursor: pointer;
}

</style>