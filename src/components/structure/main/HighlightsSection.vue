<template>
    <section>
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
                    icon : "fa-brands fa-facebook",
                    title : "title",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "dark",
                    button : {
                        text : "PRESS ME",
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

<style>

</style>