<template>
    <div class="card card-recipes" @click="onSelectedCard">
        <b-img class="img-card" :src="card.img"></b-img>
        <h4 class="card-recipes-title">{{card.title}}</h4>
        <p class="card-recipes-subtitle">{{card.subtitle}}</p>
    </div>
</template>

<script>
import {BImg}from "bootstrap-vue"
export default {
  name: 'RecipesCard',
  components: {
      BImg
  },
  props: {
      card: {
          type: Object
      }
  },
  methods: {
      onSelectedCard() {
          this.$emit('selectedCard', this.card)
      }
  }
}
</script>

<style scoup>
.card-recipes {
    /* width: 100%; */
    /* max-width: 120px; */
    /* min-width: 120px; */
    /* height: 300px; */
    background-color: transparent;
    border: none;
}

.img-card {
    width: 100%;
    height: 162px;
    border-radius: 20px;
    object-fit: cover;
}

.card-recipes-title {
    font-size: 12px;
    text-align: center;
    margin: 0;
    padding-top: 8px;
    font-weight: 700;
}

.card-recipes-subtitle {
    font-size: 10px;
    text-align: center;
}
</style>
