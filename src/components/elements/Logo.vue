<template>
    <div class="logo">
        <span class="colored-logo">NEX</span>GEN
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import '../../assets/styles/variables.scss';

    .logo{
        color: white;
        font-weight: bold;
        font-family: 'Fira Code', monospace;
        letter-spacing: 0.5rem;

        span {
            display: inline-block;
        }
    }

    .colored-logo {
        background-color: $logoBgColor ;
        padding: 0.5rem 0rem 0.5rem 1.4rem;
        margin-right: 0.2rem;
        border-radius: 20px 0px 0 20px;
        color: $logoMainColor;
    }

</style>