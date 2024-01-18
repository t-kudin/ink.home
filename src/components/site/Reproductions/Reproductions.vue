<script setup>
import { ref } from "vue";
import Button from "../../../components/shared/Button/Button.vue";
import ArtCard from "../../../components/shared/ArtCard/ArtCard.vue";

import catalogData from "../../../api/catalogData.json";

const tabItems = [
  { text: "Франция", tab: "France" },
  { text: "Германия", tab: "Germany" },
  { text: "Англия", tab: "England" },
];

const currentTab = ref("France");

const changeTab = (tab) => {
  currentTab.value = tab;
};
</script>

<template>
  <section id="reproductions" class="reproductions">
    <div class="container">
      <div class="reproductions__content">
        <div class="reproductions__header">
          <h2 class="reproductions__title">Репродукции</h2>
          <div class="reproductions__tabs">
            <Button
              @click="changeTab(item.tab)"
              variant="tab"
              v-for="(item, index) in tabItems"
              :key="index"
              >{{ item.text }}
            </Button>
          </div>
        </div>
        <div class="reproductions__catalog">
          <ArtCard
            v-for="(card, index) in catalogData.data[currentTab]"
            :key="index"
            :card="card"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "../../../assets/variables.scss";

.reproductions {
  margin: 70px 0;
  &__header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 30px;
  }
  &__title {
    color: $dark-blue;
    font-family: "Raleway", sans-serif;
    font-size: 40px;
    font-style: normal;
    font-weight: 500;
    line-height: 110%;
  }
  &__tabs {
    display: flex;
    align-items: center;
    gap: 32px;
  }
  &__catalog {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
  }
}
</style>
