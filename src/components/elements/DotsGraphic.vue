<template>
    <div class="dots-graphic">
        <span class="line">. . . . . . . . .</span>
        <span class="line">. . . . . . . . .</span>
        <span class="line">. . . . . . . . .</span>
        <span class="line">. . . . . . . . .</span>
    </div>
</template>

<script>
export default {

    name : "DotsGraphic"

}

</script>

<style lang="scss" scoped>
@import '../../assets/styles/generals.scss';
@import '../../assets/styles/variables.scss';

    span {
        display: block;
        line-height: 0.7rem;
        font-size: 2rem;
        letter-spacing: -3px;
        font-weight: bolder;
        color: $logoMainColor;
        opacity: 0.3;
    }

</style>