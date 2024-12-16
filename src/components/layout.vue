<template>
  <div class="layout">
    <hero />
    <why />
    <statistics />
    <compare />
    <contact />
    <overview />
    <marqueue />
    <share />
    <tariff />
    <again />
    <transfer />
    <info />
  </div>
</template>
<script setup>
import { onMounted, onUnmounted } from "vue";

import hero from "./hero.vue";
import why from "./why.vue";
import statistics from "./statistics.vue";
import contact from "./contact.vue";
import marqueue from "./marqueue.vue";
import compare from "./compare.vue";
import overview from "./overview.vue";
import share from "./share.vue";
import tariff from "./tariff.vue";
import again from "./again.vue";
import transfer from "./transfer.vue";
import info from "./info.vue";

const toBottomScroller = () => {
  const reveals = document.querySelectorAll(".reveal");

  const handleScroll = () => {
    const windowHeight = window.innerHeight;
    const revealPoint = 50;

    reveals.forEach((reveal) => {
      const revealTop = reveal.getBoundingClientRect().top;

      if (revealTop < windowHeight - revealPoint || reveal.classList.contains("open")) {
        reveal.classList.add("active", "line");
      }
    });
  };

  window.addEventListener("scroll", handleScroll);

  onUnmounted(() => {
    window.removeEventListener("scroll", handleScroll);
  });
};

onMounted(() => {
  toBottomScroller();
});
</script>
