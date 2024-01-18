<script setup>
import { computed } from "vue";

const { variant } = defineProps({
  variant: {
    type: String,
    default: "primary",
  },
  className: {
    type: String,
    default: "",
  },
});

const buttonClass = computed(() => {
  return variant + "-button";
});
</script>

<template>
  <button :class="`${buttonClass} ${className}`"><slot></slot></button>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";

.primary-button,
.promo-button,
.tab-button,
.text-button {
  font-family: "Raleway", sans-serif;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  transition: 0.3s ease;
  cursor: pointer;
}

.primary-button {
  color: $dark-green;
  padding: 20px 60px;
  border: 1px solid $dark-green;
  background: transparent;
  &:hover {
    color: $white;
    background: $dark-green;
  }
  &:focus {
    color: $dark-green;
    background: $greenish-grey;
  }
  &:active {
    color: $white;
    background: $olive-green;
    border: 1px solid $olive-green;
  }
}

.promo-button {
  color: $dark-blue;
  padding: 20px 60px;
  border: 1px solid $yellow;
  background: $yellow;
  &:hover {
    background: #faeb97;
    border: 1px solid #faeb97;
  }
  &:focus {
    background: #faeb97;
    border: 1px solid #a38314;
  }
  &:active {
    background: #d9b949;
    border: 1px solid #d9b949;
  }
}

.tab-button {
  color: $dark-blue;
  padding: 10px 20px;
  border-radius: 25px;
  background: $greenish-grey;
  border: 2px solid $greenish-grey;
  &:hover {
    color: $off-white;
    background: $dark-green;
    border: 2px solid $dark-green;
  }
  &:focus {
    color: $dark-blue;
    background: $greenish-grey;
    border: 2px solid $dark-green;
  }
  &:active {
    color: $off-white;
    background: $olive-green;
    border: 2px solid $olive-green;
  }
}

.text-button {
  color: $dark-blue;
  border: none;
  background: transparent;
  &:hover {
    color: $dark-green;
  }
  &:focus {
    color: $dark-blue;
    background: $greenish-grey;
  }
  &:active {
    color: $olive-green;
    background: transparent;
  }
}

.icon-button {
  border: none;
  background: transparent;
  cursor: pointer;
  transition: 0.3s ease;
}
</style>
