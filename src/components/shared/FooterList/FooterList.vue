<script setup>
import Button from "../../../components/shared/Button/Button.vue";
const { items } = defineProps({
  items: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <ul class="footer-list">
    <li class="footer-list__item" v-for="(item, index) in items" :key="index">
      <Button v-if="index === 0" variant="text">{{ item }}</Button>
      <template v-else>{{ item }}</template>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";
.footer-list {
  display: flex;
  flex-direction: column;
  gap: 6px;
  &__item {
    color: $light-green;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
  }
}
</style>
