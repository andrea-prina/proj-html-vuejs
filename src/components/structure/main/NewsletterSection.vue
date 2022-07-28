<template>
    <section class="bg-image">
        <div class="news-elements wrapper">
            <div class="w-40">
                <SectionTitle :titleData="sectionTitleInfo"/>
            </div>
            <div class="w-40">
                <form action="">
                    <input type="text" placeholder="Name">
                    <input type="text" placeholder="Email">
                    <input type="submit" value="SEND" class="btn btn-style1">
                </form>
            </div>
        </div>
    </section>
</template>

<script>
import SectionTitle from '../../elements/SectionTitle.vue'

export default {

    name : "NewsletterSection",
    components : {
        SectionTitle,
    },

    data : function(){
    return{
            sectionTitleInfo : {
                smallTitle : "Newsletter",
                preHighlightTitle : "",
                highlightTitle : "Know",
                postHighlightTitle : "First",
                paragraph : "lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem",
                style : "dark",
                button : {
                    text : "",
                    url : ""
                }
            }
        }
    },
}
</script>

<style lang="scss" scoped>
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';
@import '../../../assets/styles/buttons.scss';

    .news-elements {
        display: flex;
        justify-content: center;
        gap: 2rem;
    }

    .bg-image {
        background-image: url("../../../assets/img/bg-1.jpg");
        background-size: cover;
        background-position: center;
    }

    .w-40 {
        width: 40%;
    }

    input[type="text"]{
        width: 100%;
        height: 2.5rem;
        margin-bottom: 1rem;
        padding: 0.5rem;
        opacity: 0.6;
    }

</style>