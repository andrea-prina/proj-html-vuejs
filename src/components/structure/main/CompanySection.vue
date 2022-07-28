<template>
    <section class="flex-between">

        <div class="w-50 half-wrapper">
            <SectionTitle :titleData="sectionTitleInfo"/>

            <div class="flex-between flex-wrap mini-cards-portion">
                <div class="mini-card">
                    <h3><i class="fa-solid fa-award text-icon"></i>Tradition</h3>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
                </div>
                <div class="mini-card">
                    <h3><i class="fa-solid fa-lock text-icon"></i>Security</h3>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
                </div>
                <div class="mini-card">
                    <h3><i class="fa-solid fa-file-signature text-icon"></i>Certificate</h3>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
                </div>
                <div class="mini-card">
                    <h3><i class="fa-solid fa-graduation-cap text-icon"></i>Expertise</h3>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
                </div>
            </div>
        </div>

        <div class="w-50">
            <img src="../../../assets/img/about-3.jpg" alt="">
        </div>
    </section>
</template>

<script>
import SectionTitle from '../../elements/SectionTitle.vue'

export default {

    name : "CompanySection",

    components : {
        SectionTitle,
    },

    data : function(){
        return{
            sectionTitleInfo : {
                smallTitle : "About the network",
                preHighlightTitle : "The",
                highlightTitle : "Company",
                postHighlightTitle : "",
                paragraph : "lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem",
                style : "light",
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

    section {
        padding: 0;
        background-color: $bgc2;
    }

    .w-50 {
        width: 50%;
    }

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .half-wrapper {
        width: 80%;
        max-width: 500px;
        margin: 6rem 0 6rem auto;
        padding-right: 2rem;
    }

    .mini-cards-portion {
        margin-top: 4rem;
        gap: 1rem;
    }

    .mini-card {
        width: calc((100% - 1rem * 2 * 2) / 2);
        margin: 1rem 0rem;

        h3 {
            margin-bottom: 1rem;
        }
    }

</style>