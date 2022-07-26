<template>
    <div>
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

    a {
        color: white;
    }


</style>