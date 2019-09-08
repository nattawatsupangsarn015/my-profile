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
        var $w = $(window).scroll( function(event) {
            if($w.scrollTop() > 100){
                $(".scroll-position")
                .css({
                    "display": "flex",
                    "justify-content": "flex-end",
                    "align-items": "center"
                });
            }
            else {
                $(".scroll-position")
                .css({
                    "display": "none"
                });
            }
        });
        // this.$nextTick(this.updatePackageDom);
    },
    methods: {
        goHeader() {
            $('html, body').animate({
                scrollTop: $("#header-frame-md").offset().top
            }, 500);
        },
        goContent() {
            $('html, body').animate({
                scrollTop: $("#content-frame-md").offset().top
            }, 500);
        },
        goFooter() {
            $('html, body').animate({
                scrollTop: $("#footer-frame-md").offset().top
            }, 500);
        }
    }
}
</script>

<style scoped>

.scroll-position {
    position: fixed;
    display: none;
    justify-content: flex-end;
    align-items: center;
    height: 100vh;
    right: 6rem;
    animation: fadeIn 0.3s ease-in;
}

@keyframes fadeIn {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}

@keyframes fadeOut {
    0% {
        opacity: 1;
    }
    100% {
        opacity: 0;
    }
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