<template>
    <section id="header-frame-md" class="hidden-sm-and-down header-frame">
        <!-- <div class="change-language">
        </div> -->
        <div class="learn-more-mouse-frame">
            <div class="learn-more-mouse">
                <img src="/mouse.png" class="img-mouse">
                <div class="full-arrow">
                    <div class="line-arrow"/>
                    <div class="arrow-down"/>
                </div>
                <div class="text-scroll">
                    SCROLL
                </div>
            </div>
        </div>
        <div class="header-content-frame">
            <div class="header-content">
                <h1>NATTAWAT</h1> 
                <h1>SUPANGSARN</h1>
                <h2>FRONT-END DEVELOPER</h2>
                <div class="icon-contact-frame">
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
                <div class="learn-more">
                    <!-- <div class="learn-more-mouse">
                        <img src="/mouse.png" class="img-mouse">
                        <div class="full-arrow">
                            <div class="line-arrow"/>
                            <div class="arrow-down"/>
                        </div>
                        <div class="text-scroll">
                            SCROLL
                        </div>
                    </div> -->
                    <div class="learn-more-button" @click="goContent()">LEARN MORE</div>
                </div>
            </div>
            
        </div>
        <div id="header-menu-md" class="header-menu"> 
            <div @click="backHome()" style="cursor: pointer;">NATTAWAT SUPANGSARN</div>
            <div>
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
    </section>
</template>

<script>
import $ from "jquery";

export default {
    mounted() {
        var $w = $(window).scroll( function(event) {
            var contentFrame = $("#content-frame-md").offset().top
            var heightOfHeader = $('#header-menu-md').height()

            if($w.scrollTop() > 100) {
                $('.learn-more-mouse').css({
                    'display': 'none'
                })
            }
            else {
                $('.learn-more-mouse').css({
                    'display': 'flex'
                })
            }

            if($w.scrollTop() <= (contentFrame - heightOfHeader)){
                $(".header-menu")
                .css({
                    "display": "none"
                });
            }
            else {
                $(".header-menu")
                .css({
                    "display": "flex"
                });
            }
        });
    },
    methods: {
        backHome() {
            $('html, body').animate({
                scrollTop: $("#header-frame-md").offset().top
            }, 500);
        },
        goContent() {
            $('html, body').animate({
                scrollTop: $("#content-frame-md").offset().top
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
    justify-content: center;
    align-items: center;
    font-size: 2.5rem;
    background-color: #0c1351;
    color: #be4d08;
}

.header-content-frame {
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.header-content-frame {
    display: flex;
    justify-content: flex-start;
    width: 70%;
}

.header-content h1 {
    letter-spacing: 15px;
    font-size: 4rem;
    line-height: 1em;
}

.header-content h2 {
    margin-top: 11px;
    color: #cb8812;
    letter-spacing: 5px;
    font-size: 2rem;
}

.icon-contact-frame {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 32%;
}

.icon-contact {
    width: 2rem;
    height: 2rem;
    object-fit: contain;
    margin-right: 4px;
}

.learn-more {
    width: 100%;
    display: flex;
    margin-top: 2rem;
}

.learn-more-mouse-frame {
    position: absolute;
    top: 0rem;
    left: 5rem;
    width: 3rem;
    height: 100%;
    display: flex;
    align-items: center;
    animation: animate 1.5s infinite;
}

.learn-more-mouse {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 15rem;
}

.img-mouse {
    filter: invert(100%);
    object-fit: contain;
    width: 3rem;
    height: 3rem;
}

.line-arrow {
    transform: rotate(90deg);
    width: 6rem;
    border-top: 1px solid rgba(255,255,255,1);
}

.full-arrow {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 2rem;
    height: 2.929rem;
    justify-content: space-between;
}

.arrow-down {
    border-right: 1px solid rgba(255,255,255,1);
    border-bottom: 1px solid rgba(255,255,255,1);
    width: 12px;
    height: 12px;
    transform: rotate(45deg);
    -webkit-transform: rotate(45deg);
}

.text-scroll {
    color: rgba(255,255,255,1);
    transform: rotate(90deg);
    opacity: 0.2;
    font-size: 1rem;
    letter-spacing: 5px;
}

.learn-more-button {
    /* margin-left: 3rem; */
    display: flex;
    align-items: center;
    justify-content: center;
    width: 13rem;
    height: 2.5rem;
    color: rgba(255,255,255,1);
    font-weight: 700;
    font-size: 9px;
    border: 2px solid;
    letter-spacing: 3px;
    cursor: pointer;
}

.learn-more-button:hover {
    color: #0c1351;
    background-color: #ffff;
    transition: 0.3s;
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