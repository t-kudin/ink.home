<script setup>
import Logo from "@/components/shared/Logo/Logo.vue";
import FooterList from "@/components/shared/FooterList/FooterList.vue";
import Button from "@/components/shared/Button/Button.vue";

import FacebookIcon from "@/assets/img/facebook.svg";
import InstagramIcon from "@/assets/img/instagram.svg";
import YouTubeIcon from "@/assets/img/youtube.svg";

const reproductionItems = ["Репродукции", "Франция", "Германия", "Англия"];
const newsItems = ["Новинки", "2021", "2020"];
const aboutItems = ["О нас", "Художники", "Менеджеры"];
</script>

<template>
  <footer id="footer" class="footer">
    <div class="container">
      <div class="footer__inner">
        <div class="footer__logo">
          <Logo />
          <div>
            <a href="tel:+79995435454">+7 (999) 543-54-54</a>
            <p>Мастерская</p>
          </div>
        </div>
        <div class="footer__list">
          <FooterList :items="reproductionItems" />
          <FooterList :items="newsItems" />
          <FooterList :items="aboutItems" />
        </div>
        <div>
          <div class="footer__social">
            <Button variant="icon"><FacebookIcon /></Button>
            <Button variant="icon"><InstagramIcon /></Button>
            <Button variant="icon"><YouTubeIcon /></Button>
          </div>
          <p class="footer__text">Ink. House ®</p>
          <p class="footer__text">All rights reserved</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";
.footer {
  padding: 23px 0;
  background: $grey;
  &__inner {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
  }
  &__list {
    display: flex;
    gap: 60px;
  }
  &__text {
    margin-bottom: 6px;
    color: $light-green;
    font-size: 12px;
    font-style: normal;
    font-weight: 500;
    line-height: 120%;
  }
  &__social {
    display: flex;
    align-items: center;
    gap: 30px;
    margin-bottom: 10px;
  }
  &__logo {
    display: flex;
    flex-direction: column;
    gap: 35px;
    a {
      color: $dark-blue;
      font-size: 20px;
      font-style: normal;
      font-weight: 500;
      line-height: normal;
    }
    p {
      margin-top: 8px;
      color: $light-green;
      font-size: 18px;
      font-style: normal;
      font-weight: 500;
      line-height: normal;
    }
  }
}
</style>
