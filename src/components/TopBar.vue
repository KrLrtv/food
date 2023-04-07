<template>
    <div class="d-flex align-items-center mr-2 py-3 top-bar">
        <b-input-group>
            <b-form-input class="top-bar-input"></b-form-input>
            <b-input-group-append class="d-flex btn-search">
                <b-icon icon="search"></b-icon>
            </b-input-group-append>
        </b-input-group>
        <div class="d-flex align-items-center top-bar-right">
            <b-icon icon="gear"></b-icon>
            <b-avatar variant="info" src="https://placekitten.com/200/200" class="ml-3"></b-avatar>
            <span class="user">Taylor Henandez</span>
        </div>
    </div>
</template>

<script>
import {
    BInputGroup,
    BFormInput,
    BInputGroupAppend,
    BIcon,
    BAvatar,
} from "bootstrap-vue"
//import HealthyFood from '../assets/Image/HealthyFood.svg'
//import MyLinkMenu from "../components/MyLinkMenu.vue"

export default {
  name: 'TopBar',
  components: {
    BInputGroup,
    BFormInput,
    BInputGroupAppend,
    BIcon,
    BAvatar
  },
  data() {
    return {}
  }
}
</script>

<style scoup>
.top-bar {
    column-gap: 32px;
}
.top-bar-inputBar {
    background-color: #202020;
}

.top-bar-right {
    column-gap: 16px;
}

.btn-search {
    background-color: #202020;
    align-items: center;
    padding: 0 8px;
    border-radius: 0 0.375rem 0.375rem 0;
}
.user {
    font-size: 12px;
    white-space: nowrap;
}
</style>
