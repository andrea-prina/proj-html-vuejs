<template>
    <section>
        <div class="wrapper">
            <SectionTitle :titleData="sectionTitleInfo"/>
            <!-- TODO: Fix problems with dynamic images visualization -->
            <div class="cards flex-between flex-wrap">
                <div @mouseenter="showCardDetails(index)" @mouseleave="hideCardDetails(index)"
                v-for="(card, index) in newsCards" :key="index" class="three-cols-card img-card">
                    <img src="../../../assets/img/news-1.jpg" :alt="card.altImgText">
                    <div  v-if="card.showDetails" class="news-info flex-between">
                        <div class="author">
                            <i class="fa-regular fa-user text-icon"></i>{{card.author}}
                        </div>
                        <div class="date">
                            <i class="fa-solid fa-clock text-icon"></i>{{card.publishDate}}
                        </div>
                    </div>
                    <div class="news-text">
                        <h3>{{card.title}}</h3>
                        <p v-if="card.showDetails">{{card.paragraph}}</p>
                    </div>
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
                        imgSrc : "../../../assets/img/news-1.jpg",
                        altImgText : "news-1",
                        title : "Dolor sit amet",
                        paragraph : "lorem ipsum dolor sit amet consectetur lorem ipsum dolor sit amet",
                        author : "John Doe",
                        publishDate : "2 Days ago",
                        url : "#",
                        showDetails : false,
                    },
                    {
                        imgSrc : "../../../assets/img/news-2.jpg",
                        altImgText : "news-2",
                        title : "Dolor sit amet",
                        paragraph : "lorem ipsum dolor sit amet consectetur lorem ipsum dolor sit amet",
                        author : "John Doe",
                        publishDate : "2 Days ago",
                        url : "#",
                        showDetails : false,
                    },
                    {
                        imgSrc : "../../../assets/img/news-3.jpg",
                        altImgText : "news-3",
                        title : "Dolor sit amet",
                        paragraph : "lorem ipsum dolor sit amet consectetur lorem ipsum dolor sit amet",
                        author : "John Doe",
                        publishDate : "2 Days ago",
                        url : "#",
                        showDetails : false,
                    },
                ],
            }
    },

    methods : {

        showCardDetails : function(index){
            this.newsCards[index].showDetails = true;
        },

        hideCardDetails : function(index){
            this.newsCards[index].showDetails = false;
        }
    },

}
</script>

<style lang="scss" scoped>
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';
@import '../../../assets/styles/icons.scss';

    section {
        background-color: $bgc2;
    }

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

        &:hover {
            img {
                filter: blur(2px) brightness(0.6);
                cursor: pointer;
            }
        }

    }

    .news-text {
        position: absolute;
        left: 0;
        right: 0;
        bottom: 2rem;
        padding: 0rem 1rem;
        color: $txtc1;

        h3 {
            margin-bottom: 1rem;
        }
    }

    .news-info {
        position: absolute;
        left: 2px;
        right: 2px;
        top: 2px;
        padding: 1rem;
        color: $txtc1;
    }

</style>