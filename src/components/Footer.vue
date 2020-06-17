<template>
  <div class="footer">
    <div class="copyrate">
      <span>&#169;</span> {{ date() }} Все права защищены
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    date: function() {
      return new Date().getFullYear();
    },
  }),
  methods: {},
};
</script>
<style scoped>
.copyrate {
  padding: 40px 0;
  font-family: "Roboto";
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 14px;
  color: #333333;
}
/* .footer {
  box-sizing: border-box;
} */

@media (max-width: 1024px) {
  .copyrate {
    padding: 20px 0;
    position: fixed;
    bottom: 0px;
    margin: 0 auto;
    background-color: #fff;
    width: 100%;
  }
}
</style>
