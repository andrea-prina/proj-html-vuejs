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

<style lang="scss" scoped>
@import '../../assets/styles/generals.scss';
@import '../../assets/styles/variables.scss';
@import '../../assets/styles/buttons.scss';
@import '../../assets/styles/icons.scss';

.card {

    border-radius: 10px;
    padding: 2rem;

    .card-icon, h3, p {
        margin-bottom: 1rem;
    }

    a {
        margin: 1rem 0;
        display: inline-block;
    }

    &:hover {
        transform: translate(0, -10px);
        transition: all linear 0.1s;
        cursor: pointer;
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

    &:hover {
        .card-icon, p {
            color: $txtc1;
        }
        
        .btn {
            background-color: $brandColor;
            border: 1px solid $brandColor;
            color: $txtc1;

            &:hover {
                opacity: 0.9;
            }
        }
    }

}

</style>