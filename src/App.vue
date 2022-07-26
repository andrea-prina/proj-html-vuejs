<template>
  <div id="app">
    <Header
    :contacts = "companyContacts"/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

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

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  a {
    text-decoration: none;
  }

</style>
