<template>
  <div class="main">
      <div>
        <left-menu/>
      </div>
      
      <div class="content-page">
        <top-bar/>
        <div class="title-conainer">
          <h1>HealthyFood</h1>
          <p>Happy life</p>
          <b-img class="img" :src="cucumbers" alt="Image 1"></b-img>
        </div>

        <recipes-list />
        <Sign-in/>
      </div>
      
  </div>
</template>

<script>
import LeftMenu from "../components/LeftMenu"
import TopBar from "../components/TopBar"
import cucumbers from "@/assets/Image/cucumbers.png"
import RecipesList from "@/components/RecipesList"
import {BImg}from "bootstrap-vue"
import SignIn from "../components/SignIn"

export default {
  name: 'MainPage',
   
  components: {
    LeftMenu,
    TopBar,
    RecipesList,
    BImg,
    SignIn,
  },
  computed: {
    cucumbers() {
      return cucumbers
    }
  }
}
</script>

<style scoupe>

.main {
  display: grid;
  grid-template-columns: 300px 1fr;
  gap: 32px;
}
.content-page {
  padding-right: 32px;
  max-width: 940px;
}
.my-text {
  width: 500px;
  font-size: 20px;
}
.title-conainer {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: 216px;
}
.img {
  position: absolute;
  right: 0;
  z-index: -1;
  width: 655px;
  top: -61px;
}
</style>
