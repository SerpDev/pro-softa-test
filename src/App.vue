<template>
  <div class="mainWrap">
    <Header />
    <Content />
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header";
import Content from "./components/Content";
import Footer from "./components/Footer";

export default {
  name: "App",

  components: {
    Header,
    Content,
    Footer,
  },

  data: () => ({
    message: "",
  }),
};
</script>
<style>
.mainWrap {
  text-align: center;
}
</style>
