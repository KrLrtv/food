<template>
    <div class="carddetail card-recipes">
        <div v-if="!carddetail">Выбери рецепт</div>
        <div v-else>
            <b-img class="img-card" :src="carddetail.img"></b-img>
            <h4 class="card-recipes-title">{{carddetail.title}}</h4>
            <p class="card-recipes-subtitle">{{carddetail.subtitle}}</p>
            <p cla>{{carddetail.description}}<p/>
        </div>
        
    </div>
</template>

<script>
import {BImg}from "bootstrap-vue"
export default {
  name: 'RecipesCardDetail',
  components: {
      BImg
  },
  props: {
      carddetail: {
          type: Object
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
    margin-top: 20px;
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
