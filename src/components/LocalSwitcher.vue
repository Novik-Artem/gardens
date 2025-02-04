<template>
  <div :class="$style.swither">
    <select v-model="$i18n.locale" :class="$style.select">
      <option value="en" :class="$style.option">En</option>
      <option value="pl" :class="$style.option">Pl</option>
    </select>
  </div>
</template>

<style lang="scss" module>
.swither {
  position: fixed;
  top: 3rem;
  right: 3rem;
  width: 5rem;
  height: 5rem;
  z-index: 100;
  background-color: $black;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  .select {
    font-size: 1rem;
    color: $black;
    cursor: pointer;
    text-transform: uppercase;
    border: none;
    .option {
      border: none;
      font-size: 1rem;
      color: $black;
      cursor: pointer;
    }
  }
}
</style>
