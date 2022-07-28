<template>
    <div class="price-card three-cols-card" :class="{'focused-plan' : pricingPlan.mostPopular}">
        <div v-if="pricingPlan.mostPopular" class="most-label">
            Most Popular
        </div>
        <div class="see-plan-icon">
            <a :href="pricingPlan.url"><i class="fa-solid fa-arrow-right"></i></a>
        </div>
        <div class="price-info">
            <div class="icon">
                <i :class="pricingPlan.icon"></i>
            </div>
            <h3 class="plan-name">{{pricingPlan.name}}</h3>
            <p>$<span class="price">{{pricingPlan.price}}</span> / mo</p>
        </div>
        <ul class="price-perks">
            <li v-for="(perk, index) in pricingPlan.perks" :key="index" class="flex-between">
                <span>{{perk.description}}</span>
                <span>
                    <i v-if="perk.included" class="fa-solid fa-check"></i>
                    <i v-else class="fa-solid fa-xmark"></i>
                    </span>
            </li>
        </ul>
    </div>
</template>

<script>
export default {

    name : "PriceCard",

    props : {
        pricingPlan : Object,
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/styles/generals.scss';
@import '../../assets/styles/variables.scss';

    .price-card {
        border-radius: 10px;
        background-color: $bgc2;
        position: relative;
        padding: 2rem;

        &:hover {
            cursor: pointer;

            .see-plan-icon {
                display: block;
            }
        }

        i {
            color: $brandColor;
        }
    }

    .focused-plan {
        transform: scale(1.1);
    }

    .most-label {
        position: absolute;
        top: 15px;
        left: 0;
        width: 60px;
        background-color: $brandColor;
        color: white;
        border-radius: 0px 20px 20px 0px;
        padding: 0.5rem;
        font-size: 0.75rem;
        line-height: 0.60rem;
    }

    .see-plan-icon {
        position: absolute;
        top: 15px;
        right: 10px;
        display: none;

        a {
            font-size: 1.5rem;
            color: $brandColor;
        }
    }


    .price-info {
        text-align: center;
        padding-top: 2rem;

        .icon {
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        p {
            color: $brandColor;
        }
    }

    .price {
        margin: 1rem 0rem;
        display: inline-block;
        font-size: 2rem;
        font-weight: bold;
    }

    .price-perks {
        line-height: 1.5rem;
        color: $txtc2;
        line-height: 2rem;
    }


</style>