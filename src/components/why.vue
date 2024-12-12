<script setup>
import whyLogo from "@/assets/icons/why-comp.png";
</script>
<template>
  <div class="why">
    <div class="why-section container">
      <div class="why-wrapper">
        <div class="why-subtitle">
          <h1 class="why-subtitle__title">Почему Hujjat.uz?</h1>
          <p class="why-subtitle__desc">
            Hujjat.uz - это низко затратная система обработки транзакций, которая эффективно использует информационные
            технологии для преобразования ручного и бумажного процесса оформления документов в более быструю и более
            эффективную электронную систему формирования и ведения учета. При работе в системе традиционные бумажные
            документы заменяется на электронные документы.
          </p>
        </div>
        <div class="why-actions">
          <div class="action secondary">
            Начать работу
            <div class="action-icon right">
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" fill="none">
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M13.1893 9.7481H2.25V8.2481H13.1893L8.46967 3.52843L9.53033 2.46777L16.0607 8.9981L9.53033 15.5284L8.46967 14.4678L13.1893 9.7481Z"
                  fill="white"
                />
              </svg>
            </div>
          </div>
          <div class="action primary">
            Свяжется с нами
            <div class="action-icon right">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M14.6548 10.8291H2.5V9.16246H14.6548L9.41074 3.91838L10.5893 2.73987L17.8452 9.99579L10.5893 17.2517L9.41074 16.0732L14.6548 10.8291Z"
                  fill="#084E8C"
                />
              </svg>
            </div>
          </div>
        </div>
      </div>
      <div class="why-image">
        <img :src="whyLogo" alt="phone image" />
      </div>
    </div>
  </div>
</template>
