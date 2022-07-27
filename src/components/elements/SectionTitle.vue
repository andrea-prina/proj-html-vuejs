<template>
    <div class="wrapper flex-between">
        <div class="text-portion">
            <div class="small-title">{{titleData.smallTitle}}</div>
            <h2>
                <span>{{titleData.preHighlightTitle}} </span>
                <span class="highlighted">{{titleData.highlightTitle}}</span>
                <span> {{titleData.postHighlightTitle}}</span>
            </h2>
            <p>{{titleData.paragraph}}</p>
        </div>
        <a v-if="titleData.button.text" :href="titleData.button.url" class="btn btn-style1">{{titleData.button.text}}</a>
    </div>
</template>

<script>
export default {

    name : "SectionTitle",

    props : {

        titleData : Object,
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/styles/generals.scss';
@import '../../assets/styles/variables.scss';

    .small-title {
        color: #038483;
        text-transform: uppercase;
        font-size: 0.7rem;
        font-weight: bolder;
    }

    h2 {
        font-size: 2.5rem;
        margin: 1rem 0;
    }

    .highlighted {
        background-color: rgba(114, 162, 163, 0.2);
        color: #038483;
        padding: 0.2rem 0.5rem;
        display: inline-block;
    }

    .btn {
        align-self: flex-end;
    }

</style>