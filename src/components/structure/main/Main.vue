<template>
    <main>

        <HighlightsSection/>

        <section>
            <!-- The company -->
        </section>

        <ServicesSection/>

        <section>
            <!-- Pricing -->
        </section>

        <NewsSection/>

        <NewsletterSection/>

        <section>
            <!-- Contact Us -->
        </section>


    </main>
</template>

<script>
import HighlightsSection from './HighlightsSection.vue'
import ServicesSection from './ServicesSection.vue'
import NewsSection from './NewsSection.vue'
import NewsletterSection from './NewsletterSection.vue'

export default {
    name : 'Main',
    components : {
        HighlightsSection,
        ServicesSection,
        NewsSection,
        NewsletterSection,
    },

}

</script>

<style lang="scss">

    section {
        padding: 6rem 0rem;
    }

</style>