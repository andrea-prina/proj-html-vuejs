<template>
    <main>

        <section>
            <!-- Key highlights -->
            <div class="wrapper flex-between">
                <FeatureCard v-for="(card, index) in highlightsCards" :key="index"
                :cardInfo="card"/>
            </div>
        </section>

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
import FeatureCard from './FeatureCard.vue'

export default {
    name : 'Main',
    components : {
        FeatureCard,
    },

    data : function(){
        return{
            highlightsCards : [
                {
                    icon : "fa-brands fa-facebook",
                    title : "title",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "light",
                    button : {
                        text : "PRESS ME",
                        url : ""
                    }
                },
                {
                    icon : "fa-brands fa-facebook",
                    title : "title",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "dark",
                    button : {
                        text : "",
                        url : ""
                    }
                },
                {
                    icon : "fa-brands fa-facebook",
                    title : "title",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "light",
                    button : {
                        text : "",
                        url : ""
                    }
                },
            ]
        }
    },

}
</script>

<style lang="scss">

    section {
        padding: 6rem 0rem;
    }

</style>