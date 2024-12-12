<script setup>
import Logo from "../assets/icons/footer-logo.svg";
import { reactive } from "vue";

const data = reactive([
  {
    id: 1,
    title: "Меню",
    menu: ["О нас", "Возможности", "Цены"]
  },
  {
    id: 2,
    title: "Выполнить",
    menu: ["Вход", "Регистрация", "Поддержка"]
  },
  {
    id: 3,
    title: "Контакты",
    menu: [
      "+ 998 (71) 205-84-84",
      "179 Sampson Street, Georgetown, CO 80444",
      "1949 Linda Street, West Brunswick Twp, PA 19549",
      "autumn_philips@aol.com",
      "Cut Rite Lawn Care"
    ]
  }
]);
</script>
<template>
  <div class="footer">
    <div class="footer-wrapper container">
      <div class="footer-section">
        <div class="footer-section__info">
          <div class="footer-section__info-logo">
            <img :src="Logo" alt="logo" class="footer-section__info-icon" />
            <p class="footer-section__info-desc">Cистема учёта и формирования электронных документов</p>
          </div>
          <div class="footer-section__info-wrapper" v-for="item in data" :key="item.id">
            <h2 class="footer-section__info-title">{{ item.title }}</h2>
            <ul class="footer-section__info-menus">
              <li class="footer-section__info-menu" v-for="menu of item.menu">{{ menu }}</li>
            </ul>
          </div>
        </div>
        <div class="footer-section__adver">
          <p class="footer-section__adver-name">
            © 2024 RealSoft. Все права защищены. Создано с любовью командой RealSoft!
          </p>
          <div class="footer-section__adver-lists">
            <p class="footer-section__adver-list">Лицензия</p>
            <p class="footer-section__adver-list">Условия использования</p>
            <p class="footer-section__adver-list">Блог</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
