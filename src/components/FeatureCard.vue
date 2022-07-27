<template>
    <div class="card three-cols-card">
        <div class="card-icon centered-circle-icon big-icon">
            <i class="fa-brands fa-facebook"></i>
        </div>
        <h3>Title</h3>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import '../assets/styles/generals.scss';
@import '../assets/styles/variables.scss';

.card {

    border: 1px solid yellow;

    .card-icon, h3, p {
        margin-bottom: 1rem;
    }
}

.card-icon {
    background-color: red;
}

</style>