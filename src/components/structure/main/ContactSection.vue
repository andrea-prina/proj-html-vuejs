<template>
    <section>
        <div class="wrapper flex-between">
            <div class="left-section">
                <SectionTitle :titleData="sectionTitleInfo"/>
                <form action="" class="flex-between flex-wrap">
                    <input type="text" placeholder="name">
                    <input type="text" placeholder="email">
                    <input type="phone" placeholder="Phone">
                    <select name="" id="">
                        <option value="">Option 1</option>
                        <option value="">Option 2</option>
                        <option value="">Option 3</option>
                    </select>
                    <textarea name="" id="" cols="30" rows="10" placeholder="Message"></textarea>
                    <input type="submit" value="Submit" class="btn btn-style1">
                </form>
            </div>
            <div class="right-section">
            </div>
        </div>
    </section>
</template>

<script>
import SectionTitle from '../../elements/SectionTitle.vue'

export default {

    name : "PricingSection",

    components : {
        SectionTitle,
    },

    data : function(){
        return{
            sectionTitleInfo : {
                
                smallTitle : "Send a message",
                preHighlightTitle : "Get in",
                highlightTitle : "Touch",
                postHighlightTitle : "",
                paragraph : "lorem ipsum dolor sit amet lorem ipsum dolor sit amet lorem ipsum dolor sit amet",
                style : "light",
                button : {
                    text : "",
                    url : ""
                }
            },
        }
    },

}


</script>

<style lang="scss" scoped>
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';

    .left-section {
        width: 60%;
        padding: 2rem;
    }

    .right-section {
        width: 40%;
        padding: 1rem;
    }

    form {
        gap: 1rem;
        margin-top: 3rem;

        textarea {
            width: 100%;
        }

        input[type="text"], input[type="phone"], select {
            width: calc((100% - 0.5rem * 2 * 2) / 2);
            line-height: 2rem;
        }

        input[type="text"], input[type="phone"], select, textarea {
                background-color: lightgrey;
                border-radius: 2px;
                border: 0;
        }

    }

</style>