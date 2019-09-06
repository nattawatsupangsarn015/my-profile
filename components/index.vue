<template>
    <section>
        <Scroll/>
        <Header/>
        <Content/>
        <Footer/>
    </section>
</template>

<script>
import Header from '~/components/Header/Header.vue';
import Scroll from '~/components/Scroll.vue';
import Content from '~/components/Content/Content.vue';
import Footer from '~/components/Footer/Footer.vue';

export default {
    components: {
        Header,
        Content,
        Scroll,
        Footer
    }
}
</script>