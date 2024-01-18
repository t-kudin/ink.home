<script setup>
import Button from "../Button/Button.vue";

const { card } = defineProps({
  card: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="art-card">
    <img :src="card.imgUrl" :alt="card.name" />
    <div class="art-card__about">
      <span class="art-card__author">{{ card.author }}</span>
      <h3 class="art-card__name">{{ card.name }}</h3>
      <p class="art-card__description">{{ card.description }}</p>
      <p class="art-card__price">{{ card.price }} руб</p>
      <Button class="art-card__btn">В корзину</Button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";
.art-card {
  width: fit-content;
  padding: 20px 20px 30px 20px;
  background: $grey;
  &__about {
    margin-top: 20px;
  }
  &__author {
    color: $light-green;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
  }
  &__name {
    color: $dark-blue;
    font-size: 30px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    margin: 10px 0 8px 0;
  }
  &__description {
    color: $dark-blue;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
  }
  &__price {
    margin: 30px 0 20px 0;
    color: $dark-green;
    font-size: 24px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
  }
  &__btn {
    width: 100%;
  }
}
</style>
