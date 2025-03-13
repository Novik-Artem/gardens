<template>
  <div :class="$style.swither">
    <button
      @click="changeLanguage('en')"
      v-if="$i18n.locale === 'pl'"
      :class="$style.button"
    >
      EN
    </button>
    <button
      @click="changeLanguage('pl')"
      v-if="$i18n.locale === 'en'"
      :class="$style.button"
    >
      PL
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    changeLanguage(lang) {
      this.$i18n.locale = lang;
    },
  },
};
</script>

<style lang="scss" module>
.swither {
  position: absolute;
  top: 2rem;
  right: 2rem;
  width: auto;
  padding: 1rem 2rem;
  background-color: #f5ebdd; // Чуть прозрачный фон для легкости
  border-radius: 10px;
  border: 3px solid #353535;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background-color 0.2s ease-in-out;

  &:hover {
    background-color: #dad0c2;
  }
}

.button {
  font-size: 1.5rem;
  color: #353535;
  background: transparent;
  border: none;
  cursor: pointer;
  text-transform: uppercase;
  outline: none;

  &:focus {
    outline: none;
  }
}
</style>
