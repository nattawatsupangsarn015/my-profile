<template>
    <section>
        <Header/>
        <Content/>
        <Footer/>
    </section>
</template>

<script>
import Header from '~/components/Header/Header.vue';
import Content from '~/components/Content/Content.vue';
import Footer from '~/components/Footer/Footer.vue';

export default {
    components: {
        Header,
        Content,
        Footer
    }
}
</script>