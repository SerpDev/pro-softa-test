<template>
  <header class="header">
    <v-card class="overflow-hidden">
      <div class="head">
        <div class="head-el">
          <img class="logo" src="../assets/logo.png" />
          <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        </div>
      </div>
      <v-parallax src="../assets/boy.jpg" class="imagesBoy"></v-parallax>

      <v-navigation-drawer
        class="nav"
        v-model="drawer"
        absolute
        height="100%"
        width="100%"
        style="background-color:#E8D3C1"
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
          class="list-item-group"
        >
          <i class="material-icons closeIcon" @click="drawer = !drawer"
            >clear</i
          >
          <v-list-item v-for="(item, index) in infoText" :key="index">
            <v-list-item-title class="v-li-it">{{
              item.text
            }}</v-list-item-title>
          </v-list-item>
        </v-list-item-group>

        <div class="bottomNav" width="100%">
          <div v-for="(icon, index) in arrIcons" :key="index">
            <v-btn class="btn">
              <span class="material-icons material">
                {{ icon.icon }}
              </span>
            </v-btn>
          </div>
        </div>
      </v-navigation-drawer>
    </v-card>
  </header>
</template>

<script>
export default {
  name: "Header",
  data: () => ({
    drawer: false,
    infoText: [
      { text: "Главная" },
      { text: "Обо мне" },
      { text: "Направления" },
      { text: "Видео" },
      { text: "Контакты" },
    ],
    arrIcons: [
      { icon: "phone" },
      { icon: "mail_outline" },
      { icon: "camera_alt" },
    ],
  }),
};
</script>
<style scoped>
.header {
  box-sizing: border-box;
  overflow: hidden;
  box-shadow: none;
  word-wrap: break-word;
}
.nav {
  position: fixed;
  z-index: 2000;
}
.list-item-group {
  font-family: "Playfair Display";
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 24px;
  color: #333333;
}
.bottomNav {
  display: flex;
  width: 100%;
  flex-direction: row;
  justify-content: space-around;
  flex-wrap: wrap;
  margin-left: auto;
  margin-right: auto;
  position: absolute;
  bottom: 0;
  background-color: #fff;
}
.material {
  padding: 0 5rem;
  color: #e8d3c1;
}
.logo {
  width: 92.42px;
  height: 57px;
}
.imagesBoy {
  width: 100%;
  height: 100%;
}
.head {
  position: fixed;
  z-index: 1000;
  background-color: #fff;
  width: 100%;
}
.head-el {
  display: flex;
  justify-content: space-around;
}

.v-li-it {
  margin: 30px;
}
.closeIcon {
  cursor: pointer;
  padding: 5px;
  margin-left: 200px;
  margin-top: 100px;
}
.closeIcon:hover {
  background-color: gray;
}

@media (max-width: 700px) {
  .material {
    margin: 0.5em 6em;
  }
}
</style>
