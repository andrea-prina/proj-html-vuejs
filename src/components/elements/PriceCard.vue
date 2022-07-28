<template>
    <div class="price-card three-cols-card">
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

        i {
            color: $brandColor;
        }
    }


    .price-info {
        text-align: center;

        .icon {
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        p {
            color: $brandColor;
        }

        .price {
            margin: 1rem 0rem;
            display: inline-block;
            font-size: 2rem;
            font-weight: bold;
        }

    }

    .price-perks {
        line-height: 1.5rem;
        color: $txtc2;
        line-height: 2rem;
    }


</style>