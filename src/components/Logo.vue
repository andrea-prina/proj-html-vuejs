<template>
    <div class="logo">
        <span class="colored-logo">N E X </span>G E N
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import '../assets/styles/variables.scss';

    .logo{
        color: white;
        line-height: 3rem;
        font-family: 'Fira Code', monospace;
    }

    .colored-logo {
        background-color: rgba(3, 132, 131, 0.3) ;
        padding: 0.5rem 0rem 0.5rem 1.5rem;
        border-radius: 20px 0px 0 20px;
        color: $lightAccentColor;
    }

</style>