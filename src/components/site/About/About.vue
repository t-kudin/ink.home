<script setup>
const images = [
  "/img/about/person-1.png",
  "/img/about/person-2.png",
  "/img/about/person-3.png",
];
</script>

<template>
  <section id="about" class="about">
    <div class="container">
      <div class="about__content">
        <img src="/img/about/about.png" alt="about" />
        <div class="about__inner">
          <h2 class="about__title">Наша команда</h2>
          <p class="about__text">
            Значимость этих проблем настолько очевидна, что базовый вектор
            развития позволяет оценить значение экспериментов, поражающих
            по своей масштабности и грандиозности. Мы вынуждены отталкиваться
            от того, что консультация с широким активом.
          </p>
          <div class="about__images">
            <img
              v-for="(img, index) in images"
              :key="index"
              :src="img"
              :alt="img"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";
.about {
  padding: 70px 0;
  &__content {
    display: flex;
    align-items: center;
    gap: 30px;
  }
  &__inner {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
  &__title {
    color: $dark-blue;
    font-size: 40px;
    font-style: normal;
    font-weight: 500;
    line-height: 110%;
  }
  &__text {
    color: $dark-blue;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
  }
  &__images {
    display: flex;
    align-items: center;
    gap: 30px;
  }
}
</style>
