<template>
    <div class="three-cols-card img-card">
        <img :src="require(`../../assets/img/${cardInfo.imgSrc}`)" :alt="cardInfo.altImgText">
        <div class="news-info flex-between">
            <div class="author">
                <i class="fa-regular fa-user text-icon"></i>{{cardInfo.author}}
            </div>
            <div class="date">
                <i class="fa-solid fa-clock text-icon"></i>{{cardInfo.publishDate}}
            </div>
        </div>
        <div class="news-text">
            <h3>{{cardInfo.title}}</h3>
            <p>{{cardInfo.paragraph}}</p>
        </div>
    </div>
</template>

<script>
export default {

    name : "NewsCard",
    props : {
        cardInfo : Object,
    },

}
</script>

<style lang="scss" scoped>
@import '../../assets/styles/generals.scss';
@import '../../assets/styles/variables.scss';
@import '../../assets/styles/buttons.scss';
@import '../../assets/styles/icons.scss';

    .img-card {
        padding: 0;
        text-align: center;
        position: relative;


        img {
            width: 100%;
            object-fit: cover;
            border-radius: 10px;
            filter: brightness(0.6);
        }

        &:hover {
            img {
                filter: blur(2px) brightness(0.4);
                cursor: pointer;
            }

            .news-text p {
                display: block;
            }

            .news-info {
                display: flex;
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

        p {
            display: none;
        }
    }

    .news-info {
        position: absolute;
        left: 2px;
        right: 2px;
        top: 2px;
        padding: 1rem;
        color: $txtc1;
        display: none;
    }

</style>