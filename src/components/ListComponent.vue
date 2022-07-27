<template>
    <div class="list-component">
        <h3>{{listTitle}}</h3>
        <ul class="unstyled-list">
            <li v-for="(link, index) in listLinks" :key="index">
                <i class="fa-solid fa-angle-right text-icon"></i><a :href="link.url"> {{link.title}}</a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {

    props : {
        listTitle : String,
        listLinks : Object,
    }

}
</script>

<style lang="scss">
@import '../assets/styles/generals.scss';

    .list-component {
        padding: 2rem;
        background-color: darkslateblue;
        border-radius: 5px;
        line-height: 1.5rem;

        h3 {
            margin-bottom: 1rem;
        }
    }

    a {
        color: white;
    }


</style>