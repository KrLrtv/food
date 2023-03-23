<template>
  
    <div>
      <b-navbar toggleable="lg" type="dark" variant="primary">
        <b-container>
        <b-navbar-brand href="#">
          <b-icon-arrow-up></b-icon-arrow-up>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item href="#">Рецепты</b-nav-item>
            <b-nav-item href="#" >Disabled</b-nav-item>
          </b-navbar-nav>

        
        </b-collapse>
        </b-container>
      </b-navbar>
    </div>

</template>

<script>
import {
  BNavbar, 
  BCollapse, 
  BNavbarNav, 
  // BNavItemDropdown,
  // BDropdownItem,
  // BNavForm,
  // BButton,
  // BNavbarBrand,
  // BFormInput,
  BContainer,
  BIconArrowUp,
} from "bootstrap-vue"

export default {
  name: 'MainPage',
  components: {
    BNavbar,
    BCollapse, 
    BNavbarNav, 
    // BNavItemDropdown,
    // BDropdownItem,
    // /BNavForm,
    // BButton,
    // BNavbarBrand,
    // BFormInput,
    BContainer,
    BIconArrowUp,
  }
}
</script>

<style>
</style>
