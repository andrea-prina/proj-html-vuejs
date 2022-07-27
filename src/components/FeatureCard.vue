<template>
    <div class="card three-cols-card">
        <div class="card-icon centered-circle-icon big-icon">
            <i :class="cardInfo.icon"></i>
        </div>
        <h3>{{cardInfo.title}}</h3>
        <p>{{cardInfo.paragraph}}</p>
        <a v-if="cardInfo.button.text" class="btn btn-style1" href="">{{cardInfo.button.text}}</a>
    </div>
</template>

<script>
export default {

    name : "FeatureCard",
    props : {
        cardInfo : Object,
    }

}
</script>

<style lang="scss">
@import '../assets/styles/generals.scss';
@import '../assets/styles/variables.scss';

.card {

    border: 1px solid yellow;

    .card-icon, h3, p {
        margin-bottom: 1rem;
    }
}

.card-icon {
    background-color: red;
}

</style>