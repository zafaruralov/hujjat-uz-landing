<script setup>
import { reactive } from "vue";
import HamkorBank from "../assets/icons/HamkorBank.png";
import AloqaBank from "../assets/icons/AloqaBank.png";
import InfinBank from "../assets/icons/InfinBank.png";
import SQB from "../assets/icons/SQB.png";

const data = reactive([
  {
    id: 1,
    image: SQB
  },
  {
    id: 2,
    image: InfinBank
  },
  {
    id: 3,
    image: AloqaBank
  },
  {
    id: 4,
    image: HamkorBank
  }
]);
</script>
<template>
  <section className="marqueue">
    <div class="marqueue-text">
      <div class="compare-subtitle container">
        <h1 class="compare-subtitle__title">Hujjat.uz уже пользуются</h1>
        <p class="marqueue-title">Платформа нацелена на работу с физическими а так же с юридическими лицами</p>
      </div>
    </div>
    <div className="marqueue-wrapper">
      <div className="marqueue-group">
        <div class="marqueue-group__container" v-for="item in data" :key="item.id">
          <img :src="item.image" alt="queue-images" aria-label="supports image" />
        </div>
      </div>
      <div aria-hidden="true" className="marqueue-group">
        <div class="marqueue-group__container" v-for="item in data" :key="item.id">
          <img :src="item.image" alt="queue-images" aria-label="supports image" />
        </div>
      </div>
      <div aria-hidden="true" className="marqueue-group">
        <div class="marqueue-group__container" v-for="item in data" :key="item.id">
          <img :src="item.image" alt="queue-images" aria-label="supports image" />
        </div>
      </div>
    </div>
  </section>
</template>
