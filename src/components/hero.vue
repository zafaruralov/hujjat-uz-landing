<template>
  <div class="hero">
    <div class="hero-wrapper container">
      <div class="hero-section">
        <h1 class="hero-section__title">Hujjat.uz - Система отправки и получения электронных документов</h1>
        <p class="hero-section__desc">
          При работе в системе традиционные бумажные документы заменяется на электронные документы, что устраняет многие
          из его недостатков, при этом сохраняя документы в неизменном виде.
        </p>
      </div>
      <div class="hero-background">
        <img src="@/assets/icons/hujjat-background.png" alt="" />
      </div>
      <div class="hero-actions">
        <div class="hero-action" :style="{ animationDelay: `${0.5 * index}s` }" v-for="item in actions" :key="item.id">
          <img :src="item.icon" alt="hero icons" />
          <p class="hero-action__desc">{{ item.desc }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { reactive } from "vue";
import shield from "@/assets/icons/shield-ok.svg";

const actions = reactive([
  {
    id: 1,
    desc: "Надежность",
    icon: shield
  },
  {
    id: 1,
    desc: "Скорость",
    icon: shield
  },
  {
    id: 1,
    desc: "Удобство",
    icon: shield
  },
  {
    id: 1,
    desc: "дешево",
    icon: shield
  }
]);
</script>
