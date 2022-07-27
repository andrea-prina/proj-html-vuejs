<template>
    <section>
        <div class="wrapper">
            <SectionTitle :titleData="sectionTitleInfo"/>
            <!-- TODO: Fixare visualizzazione -->
            <div class="cards flex-between flex-wrap">
                <div v-for="(card, index) in newsCards" :key="index" class="three-cols-card img-card">
                    <img src="../../../assets/img/news-2.jpg" :alt="card.altImgText">
                    <h3>{{card.text}}</h3>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import SectionTitle from '../../elements/SectionTitle.vue'

export default {

    name : "NewsSection",
    components : {
        SectionTitle,
    },

    data : function(){
        return{
                sectionTitleInfo : {
                    smallTitle : "Our editorial content",
                    preHighlightTitle : "Latest",
                    highlightTitle : "News",
                    postHighlightTitle : "",
                    paragraph : "lorem ipsum dolor sit amet lorem ipsum dolor sit amet",
                    style : "light",
                    button : {
                        text : "SEE ALL",
                        url : "#"
                    }
                },

                newsCards : [
                    {
                        imgSrc : "../../../assets/img/news-2.jpg",
                        altImgText : "news-1",
                        text : "Lorem ipsum, dolor sit amet consectetur",
                        url : "#",
                    },
                    {
                        imgSrc : "../../../assets/img/news-2.jpg",
                        altImgText : "news-2",
                        text : "Dolor sit amet",
                        url : "#",
                    },
                    {
                        imgSrc : "../../../assets/img/news-3.jpg",
                        altImgText : "news-3",
                        text : "Lorem ipsum, dolor sit amet consectetur",
                        url : "#",
                    },
                ]
            }
    },

}
</script>

<style lang="scss" scope>
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';

    .cards {
        margin-top: 1rem;
    }

    .img-card {
        padding: 0;
        text-align: center;
        position: relative;

        img {
            width: 100%;
            object-fit: cover;
            border-radius: 10px;
        }

        h3 {
            color: white;
            position: absolute;
            left: 0;
            right: 0;
            bottom: 2rem;
            padding: 0rem 1rem;
        }
    }

</style>