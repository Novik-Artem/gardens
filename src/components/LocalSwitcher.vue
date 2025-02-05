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

.select {
  font-size: 1.5rem;
  color: #353535;
  background: transparent;
  border: none;
  cursor: pointer;
  text-transform: uppercase;
  outline: none;
  appearance: none;

  &:focus {
    outline: none;
  }
}

.option {
  font-size: 1rem;
  color: #333;
}
</style>
