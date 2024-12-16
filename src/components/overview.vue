<script setup>
import { reactive, ref } from "vue";
import OverView from "../assets/icons/overview-tag.svg";
import OverViewSpeed from "../assets/icons/overview-speed.svg";
import OverViewDescound from "../assets/icons/overview-discount.svg";
import OverViewDashboard from "../assets/icons/overview-dashboard-2.png";

let activeContainer = ref(1);
const data = reactive([
  {
    id: 1,
    title: "Сократить расходы на управление документами",
    desc: "Снижение затрат на ручное управление документами за счет оптимизации численности персонала, снижения затрат на печать, копирование и техническую поддержку других устройств.",
    image: OverView
  },
  {
    id: 2,
    title: "Оптимизация затрат на ввод данных",
    desc: "Оптимизация затрат на включение первичных учетных документов и формирование регистров, содержащих обобщенные данные.",
    image: OverViewSpeed
  },
  {
    id: 3,
    title: "Сократить время для обмена документами",
    desc: "Сократить время обработки документов с деловыми партнерами, заключить контракты, решить оперативные вопросы.",
    image: OverViewDescound
  }
]);
function toggleActiveContainer(id) {
  activeContainer.value = id;
}
</script>
<template>
  <div class="overview">
    <div class="overview-wrapper container">
      <div class="overview-section">
        <div class="compare-subtitle">
          <h1 class="compare-subtitle__title reveal">Обзор платформы</h1>
          <p class="overview-section__title reveal right">
            При работе в системе традиционные бумажные документы заменяется на электронные документы, что устраняет
            многие из его недостатков, при этом сохраняя документы в неизменном виде.
          </p>
        </div>
        <div class="overview-container">
          <img :src="OverViewDashboard" alt="OverViewDashboard" class="overview-container__icon reveal" />
          <div class="overview-container__sections">
            <div
              v-for="item in data"
              :key="item.id"
              :class="`overview-container__section ${activeContainer === item.id ? 'active' : ''}`"
              @click="toggleActiveContainer(item.id)"
            >
              <img :src="item.image" alt="section icon" class="overview-container__section-icon" />
              <div class="overview-container__section-subtitle">
                <h3 class="overview-container__section-title">
                  {{ item.title }}
                </h3>
                <p class="overview-container__section-desc">
                  {{ item.desc }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
