<template>
    <section>
        <div class="wrapper">
            <SectionTitle :titleData="sectionTitleInfo"  class="center-title"/>
        </div>
    </section>
</template>

<script>
import SectionTitle from '../../elements/SectionTitle.vue'

export default {

    name : "PricingSection",

    components : {
        SectionTitle,
    },

    data : function(){
        return{
            sectionTitleInfo : {
                
                smallTitle : "Monthly plns",
                preHighlightTitle : "Pricing",
                highlightTitle : "Table",
                postHighlightTitle : "",
                paragraph : "lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet",
                style : "light",
                button : {
                    text : "",
                    url : ""
                }
            },

        }
    }

}
</script>

<style lang="scss" scoped>
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';

    .center-title {
        justify-content: center;
        text-align: center;
        padding: 0rem 10rem;
    }

</style>