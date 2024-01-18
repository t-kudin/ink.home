<script setup>
import Button from "../../../components/shared/Button/Button.vue";
</script>

<template>
  <section id="hero" class="hero">
    <div class="container">
      <div class="hero__content">
        <img src="/img/hero-bird.jpg" alt="bird-picture" />
        <div>
          <h2 class="hero__title">Реплики картин от <span>Ink. House</span></h2>
          <p class="hero__text">
            Высокое качество отрисовки на плотной бумаге или льняном холсте.
            Редкие произведения, доступные цены.
          </p>
          <Button :variant="text">Продукция</Button>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";

.hero {
  &__content {
    display: flex;
    align-items: center;
    gap: 30px;
  }
  &__title {
    color: $dark-blue;
    font-size: 60px;
    font-style: normal;
    font-weight: 500;
    line-height: 110%;
    span {
      color: $dark-green;
    }
  }
  &__text {
    margin: 20px 0 60px 0;
    color: $light-green;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
  }
}
</style>
