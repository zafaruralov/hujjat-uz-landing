<script setup>
import { reactive, ref } from "vue";

let active = ref(2);
let isModalOpen = ref(true);

function toggleActive(id) {
  active.value = id;
}
function toggleModal() {
  isModalOpen.value = !isModalOpen.value;
}

const data = reactive([
  {
    id: 1,
    title: "Начальный",
    limit: "До 15 документов в месяц",
    desc: `Предназначен для индивидуальных пользователей или небольших компаний с минимальной потребностью в документообороте. При превышении 15 документов тариф автоматически меняется на "Базовый".`,
    price: "Бесплатно"
  },
  {
    id: 2,
    title: "Базовый",
    limit: "16-150 документов в месяц",
    desc: `Подходит для пользователей со средней нагрузкой. При отправке менее 15 документов в месяц тариф возвращается на "Начальный". При превышении 150 документов тариф меняется на "Расширенный".`,
    price: "600 сум / документ"
  },
  {
    id: 3,
    title: "Расширенный",
    limit: "151-1800 документов в месяц",
    desc: `Идеальный выбор для растущих компаний с увеличивающимся объемом документооборота. Если отправлено менее 150 документов, тариф автоматически возвращается на "Базовый". При превышении 1200 документов тариф меняется на "Профессиональный".`,
    price: "500 сум / документ"
  },
  {
    id: 4,
    title: "Корпоративный",
    limit: "1 800+ документов в месяц",
    desc: `Идеальное решение для крупных корпораций с высокими потребностями в документообороте. При отправке менее 1 800 документов тариф автоматически меняется на "Расширенный".`,
    price: "400 сум / документ"
  }
]);
</script>
<template>
  <div class="tariff">
    <div class="tariff-wrapper container">
      <div class="tariff-section">
        <div class="tariff-subtitle">
          <h1 class="tariff-subtitle__title reveal">Тарифные планы</h1>
          <p class="tariff-subtitle__desc reveal right">
            Наши тарифные планы станут доступны с 1 января 2025 года. Следите за новостями, чтобы выбрать подходящий
            вариант!
          </p>
        </div>
        <div class="tariff-sections">
          <div
            class="tariff-container"
            :class="active === item.id ? 'active' : ''"
            @click="toggleActive(item.id)"
            v-for="item in data"
            :key="item.id"
          >
            <div class="tariff-container__text">
              <div class="tariff-container__subtitle">
                <h1 class="tariff-container__subtitle-title">
                  {{ item.title }}
                </h1>
                <div
                  v-if="item.id === 2"
                  class="tariff-container__subtitle-wrapper"
                  :class="active !== item.id ? 'active' : ''"
                >
                  <div class="tariff-container__subtitle-icon">
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="16"
                      height="17"
                      viewBox="0 0 16 17"
                      fill="currentColor"
                      stroke="currentColor"
                    >
                      <path
                        d="M6.10203 4.1016C6.94646 2.58676 7.36868 1.82935 7.99992 1.82935C8.63116 1.82935 9.05338 2.58676 9.89781 4.10159L10.1163 4.4935C10.3562 4.92397 10.4762 5.1392 10.6633 5.28122C10.8504 5.42323 11.0834 5.47595 11.5493 5.58138L11.9736 5.67736C13.6133 6.04838 14.4332 6.23389 14.6283 6.86117C14.8234 7.48844 14.2644 8.14206 13.1465 9.44929L12.8573 9.78749C12.5396 10.159 12.3808 10.3447 12.3093 10.5745C12.2379 10.8043 12.2619 11.0521 12.3099 11.5477L12.3537 11.9989C12.5227 13.7431 12.6072 14.6151 12.0965 15.0028C11.5858 15.3905 10.8181 15.037 9.2828 14.3301L8.88559 14.1472C8.4493 13.9464 8.23115 13.8459 7.99992 13.8459C7.76868 13.8459 7.55054 13.9464 7.11424 14.1472L6.71703 14.3301C5.1817 15.037 4.41404 15.3905 3.90335 15.0028C3.39267 14.6151 3.47717 13.7431 3.64618 11.9989L3.68991 11.5477C3.73794 11.0521 3.76195 10.8043 3.69049 10.5745C3.61904 10.3447 3.4602 10.159 3.14253 9.78749L2.85332 9.4493C1.73542 8.14206 1.17647 7.48844 1.37153 6.86117C1.5666 6.23389 2.38649 6.04838 4.02628 5.67736L4.45051 5.58138C4.91649 5.47595 5.14947 5.42323 5.33655 5.28122C5.52362 5.1392 5.6436 4.92397 5.88356 4.4935L6.10203 4.1016Z"
                        fill="url(#paint0_linear_1585_13097)"
                      />
                      <defs>
                        <linearGradient
                          id="paint0_linear_1585_13097"
                          x1="3.53325"
                          y1="3.72935"
                          x2="12.2333"
                          y2="13.496"
                          gradientUnits="userSpaceOnUse"
                        >
                          <stop stop-color="#084E8C" />
                          <stop offset="1" stop-color="#097BE0" />
                        </linearGradient>
                      </defs>
                    </svg>
                  </div>
                  <div class="tariff-container__subtitle-text">Рекомендуется</div>
                </div>
              </div>
              <li class="tariff-container__limit">
                {{ item.limit }}
              </li>
              <p class="tariff-container__desc">
                {{ item.desc }}
              </p>
            </div>
            <div class="tariff-container__actions">
              <h1 class="tariff-container__actions-price">
                {{ item.price }}
              </h1>
              <div @click="toggleModal" class="action" :class="active === item.id ? 'primary white' : ' secondary'">
                Выбор тарифа
                <div class="action-icon right">
                  <svg
                    v-if="active !== item.id"
                    xmlns="http://www.w3.org/2000/svg"
                    width="18"
                    height="18"
                    viewBox="0 0 18 18"
                    fill="none"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M13.1893 9.7481H2.25V8.2481H13.1893L8.46967 3.52843L9.53033 2.46777L16.0607 8.9981L9.53033 15.5284L8.46967 14.4678L13.1893 9.7481Z"
                      fill="white"
                    />
                  </svg>
                  <svg v-else xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 19 19" fill="none">
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M13.6893 10.2462H2.75V8.74615H13.6893L8.96967 4.02648L10.0303 2.96582L16.5607 9.49615L10.0303 16.0265L8.96967 14.9658L13.6893 10.2462Z"
                      fill="#2B3674"
                    />
                  </svg>
                </div>
              </div>
            </div>
          </div>
          <div class="tariff-integration reveal right">
            <div class="tariff-integration__subtitle">
              <div class="tariff-container__subtitle">
                <h1 class="tariff-container__subtitle-title">Интеграционный</h1>
              </div>
              <li class="tariff-container__limit">Интеграция платформ</li>
              <p class="tariff-container__desc tarrif-txt">
                Предоставляет возможность интеграции вашей платформы с Hujjat для автоматической генерации электронных
                документов. Включает индивидуальную настройку и поддержку интеграции. Цена обсуждается отдельно.
              </p>
            </div>
            <div class="tariff-integration__actions">
              <div class="tariff-integration__action">
                <p class="tariff-integration__action-price">Цена:</p>
                <h1 class="tariff-integration__action-title">Обсуждается</h1>
              </div>
              <div class="action secondary">Свяжитесь с нами</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div v-if="isModalOpen" class="modal">
    <div class="modal-wrapper">
      <h3 class="modal-text">
        Наши тарифные планы станут доступны с 1 января 2025 года. Следите за новостями, чтобы выбрать подходящий
        вариант!
      </h3>
      <div class="modal-quit" @click="toggleModal" />
    </div>
  </div>
</template>
