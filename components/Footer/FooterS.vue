<template>
    <section id="footer-frame-xs" class="hidden-sm-and-up footer-frame">
        <div class="img-background-frame">
            <img src="/pawprint.png" class="img-background" />
        </div>
        <div class="footer-content-xs">
            <h1>THANKS FOR</h1>
            <h1>STOPPING BY !</h1>
            <div class="footer-contact-frame">
                <div class="footer-contact">
                    <a href="mailto:nattawatsupangsarn@gmail.com" target="_blank" class="email-button">
                        EMAIL ME
                    </a>
                    <div class="text-button"> OR </div>
                    <a href="https://www.linkedin.com/in/nattawatsupangsarn/" target="_blank" class="contact-button">
                        LET'S CONNECT!
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import $ from 'jquery';

export default {
    mounted() {
        var footerFrame = $('#footer-frame-xs').offset().top
        
        var $w = $(window).scroll( function(event) {
            if($w.scrollTop() >= (footerFrame - 200)){
                $('.footer-content-xs').addClass("add-animation-footer-xs");
                $('.footer-content-xs').css({
                    'display': 'flex'
                })
            }
        });
    }
}
</script>

<style scoped>

@keyframes fadeIn  {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}

.add-animation-footer-xs {
    animation: fadeIn 1s ease-out;
}


.footer-frame {
    position: relative;
    height: 100vh;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    font-size: 2.5rem;
    background-color: #be4d08;
    color: #0c1351;
}

.img-background-frame {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    overflow: hidden;
    z-index: 0;
}

.img-background { 
    object-fit: contain;
    height: 105%;
    transform: rotate(-20deg);
    filter: grayscale(100%);
    opacity: 0.1;
}

.footer-content-xs {
    display: none;
    flex-direction: column;
    align-items: flex-end;
    padding-right: 12%;
    margin-bottom: 2rem;
    z-index: 1;
}

.footer-content h1 {
    font-size: 4.5rem;
    letter-spacing: 10px;
    line-height: 1.3em;
}

.footer-contact {
    margin-top: 3rem;
    width: 55%;
}

.email-button {
    text-decoration: none;
    font-size: 8px;
    background-color: #0c1351;
    color: rgba(255,255,255,1);
    width: 10rem;
    height: 2.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 700;
    letter-spacing: 2px;
    cursor: pointer;
}

.text-button {
    font-size: 8px;
    color: rgba(255,255,255,1);
    width: 10rem;
    height: 2.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 700;
    letter-spacing: 2px;
}

.contact-button {
    font-size: 8px;
    background-color: #0c1351;
    color: rgba(255,255,255,1);
    width: 10rem;
    height: 2.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 700;
    letter-spacing: 2px;
    text-decoration: none;
    cursor: pointer;
}

.contact-button:hover {
    box-shadow: 0px 0px 4px 0px rgba(0,0,0,0.4);
}

.contact-button:active {
    box-shadow: 0px 0px 8px 0px rgba(0,0,0,0.4);
}

.email-button:hover {
    box-shadow: 0px 0px 4px 0px rgba(0,0,0,0.4);
}

.email-button:active {
    box-shadow: 0px 0px 8px 0px rgba(0,0,0,0.4);
}

</style>
