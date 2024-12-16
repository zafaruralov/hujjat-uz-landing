<script setup>
import { reactive } from "vue";
import userFirst from "../assets/icons/again-user-first.svg";
import userSecond from "../assets/icons/again-user-second.svg";
import userThird from "../assets/icons/again-user-third.svg";
import userFourth from "../assets/icons/again-user-fourth.svg";

const data = reactive([
  {
    id: 1,
    desc: `В банковской сфере важны безопасность и точность при работе с документами. Hujjat.uz помог автоматизировать процессы, упростить взаимодействие и сократить время обработки документов.`,
    userImage: userFirst,
    name: "Миржон Разаков",
    work: "JSCB “Agrobank”"
  },
  {
    id: 2,
    desc: `Управление документами для масштабных проектов часто бывает сложным, но с Hujjat.uz стало намного легче. Система позволяет быстро обмениваться документами и контролировать процесс их согласования.`,
    userImage: userSecond,
    name: "Сардор Шарипов",
    work: "“ENTER ENGINEERING” PTE.LTD DM"
  },
  {
    id: 3,
    desc: `Hujjat.uz стал для нас отличным решением для управления документами. Мы смогли ускорить процесс подготовки и подписания документов, что особенно важно для агрокластера с большим объемом работы.`,
    userImage: userThird,
    name: "Шароф Бозоров",
    work: "“AGROCLUSTER R-TEX QORAKO’L” LLC"
  },
  {
    id: 4,
    desc: `Документооборот в текстильном бизнесе требует оперативности и точности. Благодаря Hujjat.uz мы минимизировали бумажную работу и наладили удобный процесс обмена документами между отделами.`,
    userImage: userFourth,
    name: "Баходир Бердимурадов",
    work: "“SAMARQAND KAMALAK INVEST TEKSTIL” LLC"
  }
]);
</script>
<template>
  <div class="again">
    <div class="again-wrapper container">
      <div class="again-section">
        <div class="again-subtitle">
          <h1 class="again-subtitle__title reveal">Всё ещё сомневаетесь, подходит ли наша платформа вам?</h1>
          <p class="again-subtitle__price reveal right">Почитайте что говорят о нас наши клиенты</p>
        </div>
        <div class="again-containers">
          <div class="again-container" v-for="item in data" :key="item.id">
            <div class="again-container__icon">
              <svg xmlns="http://www.w3.org/2000/svg" width="48" height="37" viewBox="0 0 48 37" fill="none">
                <path
                  d="M0 36.6927V26.5985C0 23.6193 0.560789 20.4824 1.68237 17.1878C2.80394 13.8931 4.36364 10.7387 6.36145 7.72446C8.35925 4.71022 10.7076 2.13409 13.4064 -0.00390625L21.1873 5.56892C19.0493 8.68831 17.2267 11.9479 15.7196 15.3477C14.2125 18.7475 13.4589 22.4452 13.4589 26.4408V36.6927H0ZM26.8127 36.6927V26.5985C26.8127 23.6193 27.3735 20.4824 28.4951 17.1878C29.6166 13.8931 31.1763 10.7387 33.1741 7.72446C35.172 4.71022 37.5203 2.13409 40.2191 -0.00390625L48 5.56892C45.862 8.68831 44.0394 11.9479 42.5323 15.3477C41.0252 18.7475 40.2716 22.4452 40.2716 26.4408V36.6927H26.8127Z"
                  fill="#3680FA"
                />
              </svg>
            </div>
            <p class="again-container__desc">
              {{ item.desc }}
            </p>
            <div class="again-container__border" />
            <div class="again-container__info">
              <div class="again-container__info-image">
                <img :src="item.userImage" alt="user image" />
              </div>
              <div class="again-container__info-desc">
                <h1 class="again-container__info-name">
                  {{ item.name }}
                </h1>
                <p class="again-container__info-work">
                  {{ item.work }}
                </p>
              </div>
            </div>
          </div>
          <div aria-hidden="true" class="again-container" v-for="item in data" :key="item.id">
            <div class="again-container__icon">
              <svg xmlns="http://www.w3.org/2000/svg" width="48" height="37" viewBox="0 0 48 37" fill="none">
                <path
                  d="M0 36.6927V26.5985C0 23.6193 0.560789 20.4824 1.68237 17.1878C2.80394 13.8931 4.36364 10.7387 6.36145 7.72446C8.35925 4.71022 10.7076 2.13409 13.4064 -0.00390625L21.1873 5.56892C19.0493 8.68831 17.2267 11.9479 15.7196 15.3477C14.2125 18.7475 13.4589 22.4452 13.4589 26.4408V36.6927H0ZM26.8127 36.6927V26.5985C26.8127 23.6193 27.3735 20.4824 28.4951 17.1878C29.6166 13.8931 31.1763 10.7387 33.1741 7.72446C35.172 4.71022 37.5203 2.13409 40.2191 -0.00390625L48 5.56892C45.862 8.68831 44.0394 11.9479 42.5323 15.3477C41.0252 18.7475 40.2716 22.4452 40.2716 26.4408V36.6927H26.8127Z"
                  fill="#3680FA"
                />
              </svg>
            </div>
            <p class="again-container__desc">
              {{ item.desc }}
            </p>
            <div class="again-container__border" />
            <div class="again-container__info">
              <div class="again-container__info-image">
                <img :src="item.userImage" alt="user image" />
              </div>
              <div class="again-container__info-desc">
                <h1 class="again-container__info-name">
                  {{ item.name }}
                </h1>
                <p class="again-container__info-work">
                  {{ item.work }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
