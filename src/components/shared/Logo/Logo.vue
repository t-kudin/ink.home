<script setup></script>

<template>
  <a href="/" class="logo">
    <img src="/img/logo.svg" alt="logo" />
    Ink. House
  </a>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";
.logo {
  width: fit-content;
  display: flex;
  align-items: center;
  gap: 8px;
  color: $dark-green;
  font-size: 20px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}
</style>
