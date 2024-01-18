<script setup>
import Button from "../../../components/shared/Button/Button.vue";
import StarIcon from "../../../assets/img/star.svg";
</script>

<template>
  <section id="news" class="news">
    <div class="container">
      <div class="news__content">
        <h2 class="news__title">
          <StarIcon />
          Новая коллекция французских авторов
        </h2>
        <p class="news__text">
          Сложно сказать, почему акционеры крупнейших компаний призывают нас к
          новым свершениям, которые, в свою очередь, должны быть заблокированы в
          рамках своих собственных рациональных ограничений.
        </p>
        <p class="news__text">
          Принимая во внимание показатели успешности, граница обучения кадров
          предопределяет высокую востребованность направлений прогрессивного
          развития.
        </p>
        <Button className="news__btn" variant="promo">Ознакомиться</Button>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";
.news {
  padding: 70px 0;
  background: url("/img/background.png") no-repeat;
  background-size: cover;
  &__content {
    width: 555px;
  }
  &__title {
    svg {
      min-width: 80px;
    }
    display: flex;
    align-items: center;
    gap: 20px;
    color: $off-white;
    font-size: 40px;
    font-style: normal;
    font-weight: 500;
    line-height: 100%;
  }
  &__text {
    margin-top: 20px;
    color: $white;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
  }
  &__btn {
    margin-top: 60px;
  }
}
</style>
