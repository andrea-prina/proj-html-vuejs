<template>
    <section id="contact-section">
        <div class="wrapper flex-between">

            <div class="left-section">
                <SectionTitle :titleData="sectionTitleInfo"/>
                <form action="" class="flex-between flex-wrap">
                    <input type="text" placeholder="Name">
                    <input type="email" placeholder="Email">
                    <input type="phone" placeholder="Phone">
                    <select name="" id="">
                        <option value="" disabled selected>More info</option>
                        <option value="">Option 1</option>
                        <option value="">Option 2</option>
                        <option value="">Option 3</option>
                    </select>
                    <textarea name="" id="" cols="30" rows="5" placeholder="Message"></textarea>
                    <input type="submit" value="SEND" class="btn btn-style1">
                </form>
            </div>

            <div class="right-section">
                <h3>Example .inc</h3>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatum unde dolor accusamus quidem reiciendis, quasi inventore, placeat.</p>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatum unde dolor accusamus quidem reiciendis, quasi inventore, placeat.</p>
                <ul class="unstyled-list">
                    <li>
                        <span class="centered-circle-icon small-icon"><i class="fa-solid fa-phone"></i></span>{{contacts.phone}}
                    </li>
                    <li>
                        <span class="centered-circle-icon small-icon"><i class="fa-solid fa-envelope"></i></span>{{contacts.mail}}
                    </li>
                    <li>
                        <span class="centered-circle-icon small-icon"><i class="fa-solid fa-location-dot"></i></span> {{contacts.address}}
                    </li>
                </ul>
                <a href="#" class="btn btn-style3">VIEW MAP</a>
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

    props : {
        contacts : Object,
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
@import '../../../assets/styles/buttons.scss';
@import '../../../assets/styles/icons.scss';

    section {
        background-color: $bgc2;
    }

    .left-section {
        width: 60%;
        padding: 2rem;
    }

    .right-section {
        width: 40%;
        padding: 2.5rem 1rem;

        p {
            color: $txtc2;
        }

        ul {
            color: $brandColor;
        }

        span {
            background-color: $brandColorTransp;
        }

        li {
            display: flex;
            justify-content: flex-start;
            align-items: center;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .btn {
            display: inline-block;
        }

    }

    .right-section > * {
        margin-bottom: 1rem;
    }

    form {
        gap: 1rem;
        margin-top: 3rem;

        textarea {
            width: 100%;
        }

        input[type="text"], input[type="phone"], input[type="email"], select {
            width: calc((100% - 0.5rem * 2 * 2) / 2);
            height: 2.5rem;
        }

        input[type="text"], input[type="phone"], input[type="email"], select, textarea {
                background-color: $bgc5;
                padding: 0.5rem;
                border-radius: 2px;
                border: 0;
                color: grey;
        }

    }

</style>