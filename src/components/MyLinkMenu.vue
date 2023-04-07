<template>
    <b-nav-item class="my-link my-1" :active="active">
        <b-icon :icon="icon"></b-icon>
        <span class="px-2">
            {{name}}
        </span>
    </b-nav-item>
</template>

<script>
import { BNavItem, BIcon } from "bootstrap-vue"

export default {
  name: 'MyLinkMenu',
  components: {
    BNavItem,
    BIcon
  },
  props: {
      name: {
          type: String
      },
      icon: {
          type: String
      },
      active: {
          type: Boolean,
          default: false
      }
  }
}
</script>

<style scoup>
.my-link a {
  padding: 0px;
  color: #ffffff;
}
</style>
