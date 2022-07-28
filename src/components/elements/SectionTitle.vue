<template>
    <div class="flex-between">
        <div class="text-portion"
        :class="{'light-title' : titleData.style === 'light', 'dark-title' : titleData.style === 'dark'}">
            <div class="small-title">{{titleData.smallTitle}}</div>
            <h2>
                <span>{{titleData.preHighlightTitle}} </span>
                <span class="highlighted">{{titleData.highlightTitle}}</span>
                <span> {{titleData.postHighlightTitle}}</span>
            </h2>
            <p>{{titleData.paragraph}}</p>
        </div>

        <a v-if="titleData.button.text"
        :href="titleData.button.url"
        class="btn" :class="{'btn-style1' : titleData.style === 'light', 'btn-style2' : titleData.style === 'dark'}">
        {{titleData.button.text}}
        </a>

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
@import '../../assets/styles/buttons.scss';

    

    .small-title {
        color: $brandColor;
        text-transform: uppercase;
        font-size: 0.7rem;
        font-weight: bolder;
    }

    h2 {
        font-size: 2.5rem;
        margin: 1rem 0;
    }

    .highlighted {
        padding: 0.2rem 0.5rem;
        display: inline-block;
    }

    .light-title {

        color: $bgc3;

            .highlighted {
                background-color: $brandColorTransp;
                color: $brandColor;
            }

            p {
                color: $txtc2;
            }
    }

    .dark-title {
        
        color: $bgc2;

            .highlighted {
                background-color: $brandColorTransp;
                color: $txtc1;
            }

            p {
                color: $txtc2;
            }
    }

    .btn {
        align-self: flex-end;
    }

</style>