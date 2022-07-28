<template>
    <div class="card three-cols-card"
    :class="{'light-card' : cardInfo.style === 'light', 'dark-card' : cardInfo.style === 'dark'}">
        <div class="card-icon centered-circle-icon big-icon">
            <i :class="cardInfo.icon"></i>
        </div>
        <h3>{{cardInfo.title}}</h3>
        <p>{{cardInfo.paragraph}}</p>
        <a v-if="cardInfo.button.text" class="btn btn-style2" href="">{{cardInfo.button.text}}</a>
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
@import '../../assets/styles/generals.scss';
@import '../../assets/styles/variables.scss';

.card {

    border-radius: 10px;

    .card-icon, h3, p {
        margin-bottom: 1rem;
    }

    a {
        margin: 1rem 0;
        display: inline-block;
    }
}

.light-card {

    background-color: $bgc2;

    .card-icon {
        background-color: $brandColorTransp;
        color: $brandColor;
    } 

    p {
        color: darkgrey;
    }
}

.dark-card {

    background-color: $darkCard;

    .card-icon {
        background-color: $bgtrans;
        color: $brandColor;
        justify-content: flex-end;
    }

    h3 {
        color: $txtc1;
    }

    p {
        color: $txtc2;
    }

}



</style>