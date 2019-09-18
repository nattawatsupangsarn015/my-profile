<template>
    <section id="footer-frame-md" class="hidden-sm-and-down footer-frame">
        <div class="img-background-frame">
            <img src="/pawprint.png" alt="pawprint" class="img-background" />
        </div>
        <div class="footer-content">
            <h1>{{$t('thankyou1')}}</h1>
            <h1>{{$t('thankyou2')}}</h1>
            <div class="footer-contact-frame">
                <div class="footer-contact">
                    <a aria-label="email" href="mailto:nattawatsupangsarn@gmail.com" target="_blank" rel="noopener" class="email-button">
                        {{$t('emailMe')}}
                    </a>
                    <div class="text-button">{{$i18n.locale === 'en' ? 'OR' : 'หรือ'}}</div>
                    <a aria-label="linkedin" href="https://www.linkedin.com/in/nattawatsupangsarn/" target="_blank" rel="noopener" class="contact-button">
                        {{$t('letConnect')}}
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
        var footerFrame = $('#footer-frame-md').offset().top
        
        var $w = $(window).scroll( function(event) {
            if($w.scrollTop() >= (footerFrame - 200)){
                $('.footer-content').addClass("add-animation-footer");
                $('.footer-content').css({
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

.add-animation-footer {
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

.footer-content {
    display: none;
    flex-direction: column;
    align-items: flex-start;
    padding-right: 20%;
    margin-bottom: 2rem;
    z-index: 1;
}

.footer-content h1 {
    font-size: 4.5rem;
    letter-spacing: 10px;
    line-height: 1.3em;
}

.footer-contact-frame {
    width: 100%;
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

.footer-contact {
    margin-top: 3rem;
    width: 55%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.email-button {
    text-decoration: none;
    font-size: 12px;
    background-color: #0c1351;
    color: rgba(255,255,255,1);
    width: 18rem;
    height: 3rem;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 700;
    letter-spacing: 2px;
    cursor: pointer;
}

.text-button {
    font-size: 12px;
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
    font-size: 12px;
    background-color: #0c1351;
    color: rgba(255,255,255,1);
    width: 18rem;
    height: 3rem;
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
