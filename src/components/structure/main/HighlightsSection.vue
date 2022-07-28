<template>
    <section id="highlights-section">
        <div class="wrapper flex-between">
            <FeatureCard v-for="(card, index) in highlightsCards" :key="index"
            :cardInfo="card"/>
        </div>
    </section>
</template>

<script>
import FeatureCard from '../../elements/FeatureCard.vue'

export default {
    name : 'Highlights',
    components : {
        FeatureCard,
    },

    data : function(){
        return{
            highlightsCards : [
                {
                    icon : "fa-regular fa-user",
                    title : "Human Capital",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "light",
                    button : {
                        text : "",
                        url : ""
                    }
                },
                {
                    icon : "fa-solid fa-chart-pie",
                    title : "Core Business",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "light",
                    button : {
                        text : "",
                        url : ""
                    }
                },
                {
                    icon : "fa-solid fa-gauge-high",
                    title : "Performance",
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

<style lang="scss" scoped>
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';

    section {
        background-color: $bgc1;
    }

</style>