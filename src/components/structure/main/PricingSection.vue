<template>
    <section id="pricing-section">
        <div class="wrapper">
            <SectionTitle :titleData="sectionTitleInfo"  class="center-title"/>
            <div class="pricing-plans flex-between">
                <PriceCard v-for="(card, index) in pricingPlans" :key="index" :pricingPlan="card"/>
            </div>
        </div>
    </section>
</template>

<script>
import SectionTitle from '../../elements/SectionTitle.vue'
import PriceCard from '../../elements/PriceCard.vue'

export default {

    name : "PricingSection",

    components : {
        SectionTitle,
        PriceCard,
    },

    data : function(){
        return{
            sectionTitleInfo : {
                
                smallTitle : "Monthly plans",
                preHighlightTitle : "",
                highlightTitle : "Pricing",
                postHighlightTitle : "Table",
                paragraph : "lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet",
                style : "light",
                button : {
                    text : "",
                    url : ""
                }
            },

            pricingPlans : [
                    {
                        mostPopular : false,
                        icon : "fa-solid fa-rocket",
                        name : "Standard",
                        price : "490",
                        perks : [
                            {
                                description : "Standard Accounting",
                                included : true
                            },
                            {
                                description : "Platform Access",
                                included : true
                            },
                            {
                                description : "Business Orientation",
                                included : false
                            },
                            {
                                description : "Dedicated Consultant",
                                included : false
                            },
                            {
                                description : "Personal Assistance",
                                included : false
                            }
                        ]
                    },
                    {
                        mostPopular : true,
                        icon : "fa-solid fa-briefcase",
                        name : "Professional",
                        price : "890",
                        perks : [
                            {
                                description : "Standard Accounting",
                                included : true
                            },
                            {
                                description : "Platform Access",
                                included : true
                            },
                            {
                                description : "Business Orientation",
                                included : true
                            },
                            {
                                description : "Dedicated Consultant",
                                included : false
                            },
                            {
                                description : "Personal Assistance",
                                included : false
                            }
                        ]
                    },
                    {
                        mostPopular : false,
                        icon : "fa-solid fa-gem",
                        name : "Ultimate",
                        price : "1.390",
                        perks : [
                            {
                                description : "Standard Accounting",
                                included : true
                            },
                            {
                                description : "Platform Access",
                                included : true
                            },
                            {
                                description : "Business Orientation",
                                included : false
                            },
                            {
                                description : "Dedicated Consultant",
                                included : false
                            },
                            {
                                description : "Personal Assistance",
                                included : false
                            }
                        ]
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

    .center-title {
        justify-content: center;
        text-align: center;
        padding: 0rem 10rem;
    }

    .pricing-plans{
        margin-top: 3rem;
    }

</style>