<template>
  
    <div class="px-4 ms-4 mt-4 left-menu">
      
      <b-navbar-brand class="py-4" tag="h1" href="#">
        <img :src="logo" alt="HealthyFood">
      </b-navbar-brand>
      
      <div class="mt-5 menu-container mb-5 ">
        <div class="mb-2">МЕНЮ</div>
        <b-nav vertical>
          <my-link-menu 
            v-for="item in menu" 
            :key="item.name" 
            :name="item.name"
            :icon="item.icon"
          />
        </b-nav>
      </div>
      <div class="mt-5 menu-container pt-5">
        <div class="mb-2">НОВОЕ</div>
        <b-nav vertical>
          <my-link-menu 
            v-for="item in newmenu" 
            :key="item.name" 
            :name="item.name"
            :icon="item.icon"
            />
        </b-nav>
      </div>
      
    </div>

</template>

<script>
import {
  BNavbarBrand,
  BNav,
} from "bootstrap-vue"
import HealthyFood from '../assets/Image/HealthyFood.svg'
import MyLinkMenu from "../components/MyLinkMenu.vue"

export default {
  name: 'LeftMenu',
  components: {
    BNavbarBrand,
    BNav,
    MyLinkMenu,
  },
  data() {
    return {
      menu: [
        {
          name: 'Главная',
          icon: 'house-fill'
        },
                {
          name: 'Аккаунт',
          icon: 'person-fill'
        },
      ],
      newmenu: [
        {
          name: 'крем-суп',
          icon: 'circle'
        },
        {
          name: 'запечённые яблоки',
          icon: 'circle'
        },
        {
          name: 'томатный суп',
          icon: 'circle'
        }

      ]
    }
  },
  computed: {
    logo() {
      return HealthyFood
    }
  }
}
</script>

<style scoup>
.left-menu {
  background-color: transparent;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.menu-container {
  width: 100%;
  text-align: start;
}

.my-link a {
  padding: 0px;
  font-size: 14px;
}
</style>
