<script setup>
import { reactive } from "vue";

const statis = reactive([
  {
    id: 1,
    number: "70+",
    title: "подписано партнерство с платформой обмена документами."
  },
  {
    id: 2,
    number: "5,000+",
    title: "Привлечено активных пользователей."
  },
  {
    id: 3,
    number: "10,000+",
    title: "Количество документов, созданных за 1 год на платформе обмена документами."
  }
]);
</script>
<template>
  <div class="statis">
    <div class="statis-wrapper container">
      <div class="statis-section">
        <div class="statis-container" v-for="item in statis" :key="item.id">
          <h1 class="statis-container__title">{{ item.number }}</h1>
          <p class="statis-container__desc">{{ item.title }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
