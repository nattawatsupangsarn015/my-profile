<template>
    <section class="hidden-sm-and-up">
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
    methods: {
        goHeader() {
            $('html, body').animate({
                scrollTop: $("#header-frame-xs").offset().top
            }, 500);
        },
        goContent() {
            $('html, body').animate({
                scrollTop: $("#content-frame-xs").offset().top
            }, 500);
        },
        goFooter() {
            $('html, body').animate({
                scrollTop: $("#footer-frame-xs").offset().top
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
    right: 2rem;
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