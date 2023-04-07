<template>
    <div class="recipes">
        <div class="card-container">
          <h3 class="card-container-title">Top Artists</h3>
          <div class="list-card">
            <recipes-card
              v-for="card in listRecept"
              :key="card.title"
              :card="card"
              @selectedCard="selectedCard"
            />
          </div>
        </div>
        <div class="card-container">
          sdsd12345613243
          <RecipesCardDetail :carddetail="currentCard"/>
        </div>
    </div>
</template>

<script>
import img1 from '@/assets/Image/img1.jpg'
import RecipesCard from '@/components/RecipesCard'
import RecipesCardDetail from '../components/RecipesCardDetail'

import img2 from "../assets/Image/запечённые_яблоки_с_суфофруктами_и_орехами.jpeg"
import img3 from "../assets/Image/индейка_с_овощами .jpeg"
import img4 from "../assets/Image/куринный_крем_суп.jpeg"
import img5 from "../assets/Image/овсяная_каша_с_яблоком.jpeg"
import img6 from "../assets/Image/рыбацкий_суп_с_треской_и_гребешками .jpeg"
import img7 from "../assets/Image/треска_в_пергаменте_с_сальсой.jpeg"
//import черничные_маффины from "../assets/Image/черничные_маффины"
export default {
  name: 'RecipesList',
  components: {
    RecipesCard,
    RecipesCardDetail
  },
  data() {
    return {
      currentCard: null,
      listRecept: [
        { title: 'Борщ', subtitle: 'Вкусный', img: img1, description:'жидкое блюдо, в составе которого содержится не менее 50 % жидкости. Жидкую часть супа называют основой, плотную — гарниром. Супы готовят на бульонах, отварах, молоке и молочных продуктах и квасе.'},
        { title: 'Заппечённые яблоки', subtitle: 'С сухофруктами и орехами', img: img2,description:"небольшая горсть мелкого темного изюма плоды вяленого инжира – 2 шт. вяленые финики – 2 шт. по 1 ст. л. кедровых орехов, миндаля и кешью молотая корица – 1 ч. л. щепотка имбирного порошка крупные зеленые яблоки (гренни смит или симиренко) – 4 шт. жидкий мед или кленовый сироп для подачи"},
        { title: 'Индейка', subtitle: 'С овощами', img: img3, description:''},
        { title: 'Крем-суп', subtitle: 'Куриный', img: img4},
        { title: 'Овсянная каша', subtitle: 'С яблоками', img: img5},
        { title: 'Суп с треской', subtitle: 'И морскими гребешками', img: img6},
        { title: 'Треска в прегаменте', subtitle: 'С сальсой из помидоров', img: img7},
      ],
    }
  },
  methods: {
    selectedCard(card) {
      this.currentCard = card
    }
  }
}
</script>

<style scoup>
.recipes {
    display: grid;
    grid-template-columns: 1fr 300px;
    gap: 16px;
}
.card-container {
    background-color: rgba(32, 32, 32, 0.86);
    border-radius: 32px;
    padding: 16px;
}
.card-container-title {
  font-size: 16px;
  margin-bottom: 24px;
  margin-left: 10px;
}

.list-card {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 24px;
}
</style>
