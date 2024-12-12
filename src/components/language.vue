<template>
  <div class="auth__language-picker">
    <div
      class="auth__language-selected"
      :style="{ background: pickerBackground, color: textColor }"
      @click="toggleDropdown"
      v-on-click-outside="setDropdownInvisible"
    >
      {{ selectedLanguage.name }}
      <!-- <img src="@/assets/icon/arrow-down.svg" alt="arrow-down svg" :class="{ rotate: isDropdownOpen }" /> -->
    </div>
    <ul class="auth__language-list" v-if="isDropdownOpen">
      <li
        v-for="language in languages"
        :key="language.code"
        @click="selectLanguage(language)"
        class="auth__language-list-item"
      >
        {{ language.name }}
      </li>
    </ul>
  </div>
</template>

<script setup>
import { watch, onMounted, ref } from "vue";
// import { vOnClickOutside } from "@vueuse/components";

const selectedLanguage = ref("");
const isDropdownOpen = ref(false);

const props = defineProps({
  pickerBackground: String,
  textColor: String
});

const defaultLang = { code: "uz", name: "Ўзбекча" };
const storageLang = localStorage.getItem("platon_locale");

const languages = [
  { code: "uz", name: "Ўзбекча" },
  { code: "la", name: "Oʻzbekcha" },
  { code: "ru", name: "Русский" },
  { code: "en", name: "English" }
];

// onMounted(() => {
//   if (storageLang) {
//     selectedLanguage.value = languages.find((lang) => lang.code === locale.value) || storageLang;
//   } else {
//     selectLanguage(defaultLang);
//   }
// });

// watch(locale, () => {
//   selectedLanguage.value = languages.find((lang) => lang.code === locale.value) || defaultLang;
// });

function setDropdownInvisible(event, el) {
  isDropdownOpen.value = false;
}

const toggleDropdown = () => {
  isDropdownOpen.value = !isDropdownOpen.value;
};

const selectLanguage = (language) => {
  selectedLanguage.value = language;
  isDropdownOpen.value = false;

  locale.value = language.code;
  window.localStorage.setItem("platon_locale", language.code);
};
</script>
