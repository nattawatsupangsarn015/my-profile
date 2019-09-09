<template>
    <section id="header-frame-sm" class="hidden-md-and-up hidden-xs-only header-frame">
        <div class="header-content-frame">
            <h1>NATTAWAT</h1>
            <h1>SUPANGSARN</h1>
            <h2>FRONT-END DEVELOPER</h2>
            <div class="icon-header-scroll">
                <a href="https://www.linkedin.com/in/nattawatsupangsarn/" target="_blank" class="icon-link">
                    <img src="/linkedin-icon.png" class="icon-contact"/>
                </a>
                <a href="https://github.com/nattawatsupangsarn015/" target="_blank" class="icon-link">
                    <img src="/github-icon.png" class="icon-contact"/>
                </a>
                <a href="mailto:nattawatsupangsarn@gmail.com" target="_blank" class="icon-link">
                    <img src="/email-icon.png" class="icon-contact"/>
                </a>
                <a href="tel:+669322942" target="_blank" class="icon-link">
                    <img src="/phone-icon.png" class="icon-contact"/>
                </a>
            </div>
        </div>
        <div id="header-menu-sm" class="header-menu"> 
            <div @click="backHome()" style="cursor: pointer;">NATTAWAT SUPANGSARN</div>
            <div class="icon-header-scroll">
                <a href="https://www.linkedin.com/in/nattawatsupangsarn/" target="_blank" class="icon-link">
                    <img src="/linkedin-icon.png" class="icon-contact"/>
                </a>
                <a href="https://github.com/nattawatsupangsarn015/" target="_blank" class="icon-link">
                    <img src="/github-icon.png" class="icon-contact"/>
                </a>
                <a href="mailto:nattawatsupangsarn@gmail.com" target="_blank" class="icon-link">
                    <img src="/email-icon.png" class="icon-contact"/>
                </a>
                <a href="tel:+669322942" target="_blank" class="icon-link">
                    <img src="/phone-icon.png" class="icon-contact"/>
                </a>
            </div>
        </div>
        <div class="learn-more-frame">
            <div class="learn-more-mouse-frame-sm">
                <img src="/hand.png" class="img-hand"/>
            </div>
            <div @click="goContent()" class="learn-more-button">
                LEARN MORE
            </div>
        </div>
    </section>
</template>

<script>
import $ from "jquery";

export default {
    mounted() {
        var $w = $(window).scroll( function(event) {
            var contentFrame = $("#content-frame-sm").offset().top
            var heightOfHeader = $('#header-menu-sm').height()

            if($w.scrollTop() > 100) {
                $('.learn-more-mouse-frame-sm').css({
                    'display': 'none'
                })
            }
            else {
                $('.learn-more-mouse-frame-sm').css({
                    'display': 'flex'
                })
            }

            if($w.scrollTop() <= (contentFrame - heightOfHeader)){
                $("#header-menu-sm")
                .css({
                    "display": "none"
                });
            }
            else {
                $("#header-menu-sm")
                .css({
                    "display": "flex"
                });
            }
        });
    },
    methods: {
        backHome() {
            $('html, body').animate({
                scrollTop: $("#header-frame-sm").offset().top
            }, 500);
        },
        goContent() {
            $('html, body').animate({
                scrollTop: $("#content-frame-sm").offset().top
            }, 500);
        }
    }
}
</script>

<style scoped>

.header-frame {
    position: relative;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 2.5rem;
    background-color: #0c1351;
    color: #be4d08;
}

.learn-more-frame {
    position: relative;
    display: flex;
    width: 85%;
    height: 35%;
    padding-top: 3rem;
}

.learn-more-button {
    color: rgba(255,255,255,1);
    border: 2px solid;
    font-size: 9px;
    letter-spacing: 2px;
    width: 23%;
    height: 2.2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 10%;
    font-weight: 700;
}

.learn-more-button:active {
    color: #0c1351;
    background: #ffff;
    transition: 0.2s;
}

.learn-more-mouse-frame-sm {
    position: absolute;
    padding-top: 3rem;
    top: 0;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;
    width: 8%;
    animation: animate 1.5s infinite;
}

.img-hand {
    -webkit-filter: invert(100%);
    filter: invert(100%);
    transform: rotate(180deg);
    width: 2.5rem;
    height: 2.5rem;
    -o-object-fit: contain;
    object-fit: contain;
}

.header-menu {
    position: fixed;
    padding: 0rem 4rem;
    top: 0;
    display: none;
    height: 4rem;
    font-size: 1.5rem;
    width: 100%;
    justify-content: space-between;
    align-items: center;
    background-color: #0c1351;
    color: #be4d08;
    z-index: 1;
}

.icon-header-scroll {
    height: 2rem;
    width: 23%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.icon-contact {
    width: 1.5rem;
    height: 1.5rem;
    object-fit: contain;
    margin-right: 8px;
}

.header-content-frame {
    width: 85%;
    height: 35%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
}

.header-content-frame h1 {
    font-size: 2rem;
    letter-spacing: 10px;
    line-height: 1.3em;
}

.header-content-frame h2 {
    margin: 7px 0px;
    font-size: 1rem;
    letter-spacing: 10px;
    color: #cb8812;
}

@keyframes animate {
    0% { top: 0rem; }
    /* 10% { top: 0.1rem; }
    20% { top: 0.2rem; }
    30% { top: 0.3rem; }
    40% { top: 0.4rem; } */
    50% { top: 2rem; }
    /* 60% { top: 0.4rem; }
    70% { top: 0.3rem; }
    80% { top: 0.2rem; }
    90% { top: 0.1rem; } */
    100% { top: 0rem; }
}

</style>