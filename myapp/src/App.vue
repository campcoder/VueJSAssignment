<template>
  <div class="main">
    <Header />
    <h1 class="title">Body</h1>
    <div class="container">
      <Body />
    </div>
    <Footer />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Body from "./components/Body.vue";

export default {
  name: "App",
  components: {
    Header,
    Body,
    Footer,
  },
};
</script>

<style>
.container {
  padding-left: 70px;
  align-content: center;
  font-weight: bold;
}

.title {
  text-align: center;
  padding-top: 95px;
}
</style>
