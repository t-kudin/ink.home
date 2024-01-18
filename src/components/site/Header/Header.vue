<script setup>
import Logo from "../../../components/shared/Logo/Logo.vue";
import Button from "../../../components/shared/Button/Button.vue";

import CartIcon from "../../../assets/img/cart.svg";

const menuItems = [
  {
    text: "Репродукции",
    link: "reproductions",
  },
  {
    text: "Новинки",
    link: "news",
  },
  {
    text: "О нас",
    link: "about",
  },
];
</script>

<template>
  <header id="header" class="header">
    <div class="container">
      <div class="header__inner">
        <Logo />
        <nav class="header__nav">
          <a :href="`#${item.link}`" v-for="item in menuItems">
            <Button variant="text">{{ item.text }}</Button>
          </a>
          <a href="#">
            <Button variant="icon">
              <CartIcon />
            </Button>
          </a>
        </nav>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";
.header {
  padding: 32px 0;
  background: $grey;
  &__inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  &__nav {
    display: flex;
    align-items: center;
    gap: 60px;
  }
}
</style>
