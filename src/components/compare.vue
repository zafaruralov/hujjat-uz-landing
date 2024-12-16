<script setup>
import compareFirstIcon from "../assets/icons/compare-first2.png";
import compareSecondIcon from "../assets/icons/compare-second.png";
</script>
<template>
  <div class="compare">
    <div class="compare-wrapper container">
      <div class="compare-section">
        <div class="compare-subtitle reveal">
          <h1 class="compare-subtitle__title">Сравните сами</h1>
        </div>
        <div class="compare-container">
          <div class="compare-container__wrapper">
            <div class="compare-subtitle reveal">
              <p class="compare-subtitle__link">Настоящее время</p>
              <h1 class="compare-subtitle__title">Поэтапное оформление документов КАК ЕСТЬ!</h1>
              <p class="compare-subtitle__desc">
                Вывод документа с принтера, подписание документа
                <span class="compare-subtitle__desc-link">(1 день)</span>, передача курьеру для доставки, доставка
                документа курьером получателю <span class="compare-subtitle__desc-link">(1 день)</span>, подпись
                документа получателем, передача курьеру для доставки обратно
                <span class="compare-subtitle__desc-link">(1 день)</span>
              </p>
            </div>
            <div class="compare-container__wrapper-icon reveal active">
              <img :src="compareFirstIcon" alt="compareFirstIcon" />
            </div>
          </div>
          <div class="compare-container__height" />
          <div class="compare-container__wrapper">
            <div class="compare-subtitle reveal">
              <p class="compare-subtitle__link">Результат</p>
              <h1 class="compare-subtitle__title">Автоматизации процесса электронного ведения учета документов!</h1>
              <p class="compare-subtitle__desc">
                Оформление документа занимающий от <span class="compare-subtitle__desc-link">2-3х</span> дней и
                сокращает до
              </p>
            </div>
            <div class="compare-container__wrapper-icon reveal active">
              <img :src="compareSecondIcon" alt="compareSecondIcon" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang=""></style>
