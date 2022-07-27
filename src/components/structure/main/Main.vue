<template>
    <main>

        <HighlightsSection/>

        <section>
            <!-- The company -->
        </section>

        <section>
            <!-- Services -->
        </section>

        <section>
            <!-- Pricing -->
        </section>

        <section>
            <!-- News -->
        </section>

        <section>
            <!-- Newsletter -->
        </section>

        <section>
            <!-- Contact Us -->
        </section>


    </main>
</template>

<script>
import HighlightsSection from './HighlightsSection.vue'

export default {
    name : 'Main',
    components : {
        HighlightsSection,
    },

}

</script>

<style lang="scss">

    section {
        padding: 6rem 0rem;
    }

</style>