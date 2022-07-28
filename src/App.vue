<template>
  <div id="app">
    <Header
    :contacts = "companyContacts"/>
    <Main
    :contacts = "companyContacts"/>
    <Footer
    :contacts = "companyContacts"/>

    <div>
        <a href="#" class="go-top-icon centered-circle-icon big-icon">
            <i class="fa-solid fa-arrow-up"></i>
        </a>
    </div>

  </div>
</template>

<script>
import Header from './components/structure/header/Header.vue';
import Main from './components/structure/main/Main.vue';
import Footer from './components/structure/footer/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },

  data : function(){
    return {
      companyContacts : {
        phone : "+1 (305) 1234-5678",
        mail : "hello@example.com",
        address : "Main Avenue, 987"
      }
    }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Alfa+Slab+One&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@500;600&display=swap');
@import './assets/styles/variables.scss';
@import './assets/styles/icons.scss';

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    // TODO: Find font more similar to the one used in the reference picture
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    scroll-behavior: smooth;
  }

  a {
    text-decoration: none;
  }

  .go-top-icon {
    position: fixed;
    bottom: 5px;
    right: 5px;
    background-color: $bgc3;
    opacity: 0.2;

    &:hover {
        cursor: pointer;
        opacity: 0.7;
    }
  }

</style>
