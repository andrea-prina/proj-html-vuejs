<template>
    <main>

        <HighlightsSection/>

        <CompanySection/>

        <ServicesSection/>

        <PricingSection/>

        <NewsSection/>

        <NewsletterSection/>

        <section>
            <!-- Contact Us -->
        </section>


    </main>
</template>

<script>
import HighlightsSection from './HighlightsSection.vue';
import ServicesSection from './ServicesSection.vue';
import NewsSection from './NewsSection.vue';
import NewsletterSection from './NewsletterSection.vue';
import CompanySection from './CompanySection.vue';
import PricingSection from './PricingSection.vue';

export default {
    name : 'Main',
    components : {
        HighlightsSection,
        ServicesSection,
        NewsSection,
        NewsletterSection,
        CompanySection,
        PricingSection,
    },

}

</script>

<style lang="scss">

    section {
        padding: 6rem 0rem;
    }

</style>