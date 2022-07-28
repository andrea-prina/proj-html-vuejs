<template>
    <section>
        <div class="wrapper">
            <SectionTitle :titleData="sectionTitleInfo"/>
            <div class="cards flex-between flex-wrap">
                <NewsCard v-for="(card, index) in newsCards" :key="index" :cardInfo="card"/>
            </div>
        </div>
    </section>
</template>

<script>
import SectionTitle from '../../elements/SectionTitle.vue'
import NewsCard from '../../elements/NewsCard.vue'

export default {

    name : "NewsSection",
    components : {
        SectionTitle,
        NewsCard
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
                        imgSrc : "../../../assets/img/news-1.jpg",
                        altImgText : "news-1",
                        title : "Dolor sit amet",
                        paragraph : "lorem ipsum dolor sit amet consectetur lorem ipsum dolor sit amet",
                        author : "John Doe",
                        publishDate : "2 Days ago",
                        url : "#",
                    },
                    {
                        imgSrc : "../../../assets/img/news-2.jpg",
                        altImgText : "news-2",
                        title : "Dolor sit amet",
                        paragraph : "lorem ipsum dolor sit amet consectetur lorem ipsum dolor sit amet",
                        author : "John Doe",
                        publishDate : "2 Days ago",
                        url : "#",
                    },
                    {
                        imgSrc : "../../../assets/img/news-3.jpg",
                        altImgText : "news-3",
                        title : "Dolor sit amet",
                        paragraph : "lorem ipsum dolor sit amet consectetur lorem ipsum dolor sit amet",
                        author : "John Doe",
                        publishDate : "2 Days ago",
                        url : "#",
                    },
                ],
            }
    },

}

</script>

<style lang="scss" scoped>
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';
@import '../../../assets/styles/buttons.scss';
@import '../../../assets/styles/icons.scss';

    section {
        background-color: $bgc2;
    }

    .cards {
        margin-top: 1rem;
    }

</style>