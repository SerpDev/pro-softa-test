<template>
  <div class="content">
    <div class="someText">
      <span
        >Привет! Ты оказался на страничке фотографа. Когда дочитаешь до конца,
        захочешь со мной познакомиться и оказаться под прицелом моего объектива.
        Самонадеянно? Пожалуй.</span
      >
    </div>
    <div><span class="someText1">На это есть основания</span></div>

    <div class="blockStar" v-for="(item, index) in textInfo" :key="index">
      <div>
        <i class="material-icons">{{ item.icon }}</i>
        <div class="someText2">{{ item.text }}</div>
      </div>
    </div>
    <div class="infoaboutUs">
      <div class="titleAboutUs">
        Я – ТАНЯ И Я – НЕСТАТИЧНЫЙ ФОТОГРАФ.
      </div>
      <div class="someText3">
        Фотографии – это свидетельство того, что мы есть. Фотографии показывают,
        какие мы. Моменты нашей жизни надо ПРОЖИВАТЬ чувственно и с чувствами
        фиксировать. Поэтому, никаких постановок. У меня – все по-настоящему!
      </div>
    </div>
    <div class="direction">
      <div>Направления</div>
      <div class="cardHum">
        <div v-for="(item, index) in directionInfo" :key="index">
          <v-card
            max-width="300"
            class="cardd"
            @mouseenter="item.show = !item.show"
            @mouseleave="item.show = !item.show"
          >
            <v-img src="../assets/girlFoto.png" height="200px"></v-img>
            <v-card-title>
              {{ item.title }}
            </v-card-title>
            <v-card-text>
              {{ item.text1 }}
            </v-card-text>
            <v-card-actions>
              <v-btn icon>
                <v-icon>{{
                  item.show ? "mdi-chevron-up" : "mdi-chevron-down"
                }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="item.show">
                <v-divider></v-divider>

                <v-card-text>
                  I'm a thing. But, like most politicians, he promised more than
                  he could deliver. You won't have time for sleeping, soldier,
                  not with all the bed making you'll be doing. Then we'll go
                  with that data file! Hey, you add a one and two zeros to that
                  or we walk! You're going to do his laundry? I've got to find a
                  way to escape.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </div>
      </div>
    </div>
    <div class="video-wrap">
      <div class="textVideo">Видео</div>
      <div class="video">
        <div class="bllockVideo">
          <video
            controls
            width="300"
            height="165"
            poster="../assets/bg-video-girl.png"
          >
            <source src="../assets/promo3.mp4" type="video/mp4" />
          </video>
          <div class="textSomes">
            <h4>Co мной актуально</h4>
            <span>Репортажная съемка – всегда на пике событий.</span>
          </div>
        </div>
        <div class="bllockVideo">
          <video
            controls
            width="300"
            height="165"
            poster="../assets/bg-video-girl.png"
          >
            <source src="../assets/promo2.mp4" type="video/mp4" />
          </video>
          <div class="textSomes">
            <h4>Со мной выгодно</h4>
            <span
              >Промо-ролик – сделаем рекламу ваших продуктов/услуг на зависть
              всем.</span
            >
          </div>
        </div>
        <div class="bllockVideo">
          <video
            controls
            width="300"
            height="165"
            poster="../assets/bg-video-girl.png"
          >
            <source src="../assets/promo1.mp4" type="video/mp4" />
          </video>
          <div class="textSomes">
            <h4>Со мной весело</h4>
            <span
              >Вайны – юмор спасет мир! Вместе снимаем, я монтирую, все
              смеются.</span
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Content",
  data: () => ({
    url: "../assets/promo1.mp4",
    textInfo: [
      {
        text:
          "5 лет жизни  с фотоаппаратом в руках, которые точно растут не из *опы",
        icon: "star_border",
      },
      {
        text: "Целый арсенал профессиональной техники. И не с aliexpess",
        icon: "star_border",
      },
      {
        text:
          "Гигабайты фотографий, на которых есть жизнь и настоящие эмоции, а не вымученные позы.",
        icon: "star_border",
      },
      { text: "Острый взгляд  и бездна вкуса.", icon: "star_border" },
    ],

    directionInfo: [
      {
        title: "LIFESTYLE",
        text1:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ",
        show: false,
      },
      {
        title: "Портрет",
        text1:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ",
        show: false,
      },
      {
        title: "Семейная фотосессия",
        text1:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.  ",
        show: false,
      },
    ],
  }),
  methods: {},
};
</script>
<style scoped>
.someText {
  min-width: 300px;
  font-family: "Montserrat", italic;
  font-weight: 300;
  font-size: 14px;
  line-height: 18px;
  margin: 110px 25% 3% 25%;
  padding: 20px 50px;
  background: #ffffff;
  box-shadow: 2px 2px rgb(197, 196, 196), -1em -20px 2px #e8d3c1;
  word-break: break-all;
  overflow: hidden;
}
.someText1 {
  font-family: "Montserrat";
  font-weight: 500;
  font-size: 14px;
  line-height: 23px;
}
.material-icons {
  color: #e8d3c1;
  margin-bottom: 30px;
}
.blockStar {
  display: inline-flex;
  flex-wrap: wrap;
  word-wrap: break-word;
  width: 220px;
  margin: 30px;
}
.titleAboutUs {
  color: #919191;
  font-family: "Playfair Display";
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 19px;
  text-transform: uppercase;
}
.someText3 {
  font-family: Montserrat;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 19px;
  color: #333333;
  margin-top: 20px;
}
.infoaboutUs {
  max-width: 950px;
  margin: 0 auto;
  word-wrap: break-word;
}
.cardHum {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-self: center;
  flex-wrap: wrap;
  font-family: "Montserrat";
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 19px;
}
.cardd {
  margin: 20px;
}
.cardd:hover {
  cursor: pointer;
  background-color: #e8d3c1;
}
.direction,
.textVideo {
  margin: 30px 0 40px 0;
  font-family: Playfair Display;
  font-style: normal;
  font-weight: bold;
  font-size: 18px;
  line-height: 24px;
  color: #333333;
}
.video-wrap {
  background-color: #e8d3c1;
  padding-bottom: 60px;
  padding-top: 10px;
}
.video {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.bllockVideo {
  margin: 0 20px 20px 20px;
  width: 300px;
  background-color: #fff;
  box-shadow: -5px 53px 60px -8px rgba(0, 0, 0, 0.51);
}
.textSomes {
  padding: 10px;
}
h4 {
  font-family: "Playfair Display";
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 19px;
  margin-bottom: 10px;
}
span {
  font-family: "Montserrat";
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 17px;
}

@media (max-width: 700px) {
  .someText {
    padding: 20px;
    margin: 100px 40px 50px 40px;
  }
}
@media (max-width: 400px) {
  .someText {
    padding: 10px;
    margin: 100px 15px 30px 15px;
  }
}
</style>
