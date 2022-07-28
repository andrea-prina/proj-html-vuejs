<template>
    <main>

        <HighlightsSection/>

        <CompanySection/>

        <ServicesSection/>

        <PricingSection/>

        <NewsSection/>

        <NewsletterSection/>

        <ContactSection
        :contacts="contacts"/>

    </main>
</template>

<script>
import HighlightsSection from './HighlightsSection.vue';
import CompanySection from './CompanySection.vue';
import ServicesSection from './ServicesSection.vue';
import PricingSection from './PricingSection.vue';
import NewsSection from './NewsSection.vue';
import NewsletterSection from './NewsletterSection.vue';
import ContactSection from './ContactSection.vue';

export default {
    name : 'Main',
    components : {
        HighlightsSection,
        CompanySection,
        ServicesSection,
        PricingSection,
        NewsSection,
        NewsletterSection,
        ContactSection,
    },

    props : {
        contacts : Object,
    },

}

</script>

<style lang="scss">

    section {
        padding: 6rem 0rem;
    }

</style>