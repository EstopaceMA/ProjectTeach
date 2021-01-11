<template>
  <aside v-show="isAsideVisible" class="aside is-placed-left is-expanded">
    <aside-tools class="teach-logo" :is-main-menu="true">
      <span slot="label" style="font-size: xx-large">
        <b>
          Q <span style="color: #4A76C7">Teach</span>
        </b>
      </span>
    </aside-tools>
    <div class="menu is-menu-main" style="margin-top: 4rem">
      <div style="display: flex; justify-content: center;">
        <template v-for="(menuGroup, index) in menu">
          <p v-if="typeof menuGroup === 'string'" :key="index" class="menu-label">
            {{ menuGroup }}
          </p>
          <aside-menu-list
            v-else
            :key="index"
            :menu="menuGroup"
            @menu-click="menuClick"
          />
        </template>
      </div>
    </div>
  </aside>
</template>

<style >
  .teach-logo{
    background-color: transparent !important;
    margin-top: 1.5rem;
    text-align: center;
    display: block !important;
  }

  .menu-list{
    line-height: 3 !important;
  }

  .menu-list a.is-active{
    background-color: transparent;
    color: #4A76C7;
    margin-left: 0.75rem;
  }

  .menu-list a{
    color: #fff;
  }

  .menu-list a:hover{
    background-color: transparent;
    color: #4A76C7;
  }

  .aside{
    background-color: #2C3144 !important;
  }

  li .mdi{
    font-size: 1.5rem !important;
  }
</style>

<script>
import { mapState } from 'vuex'
import AsideTools from '@/components/AsideTools'
import AsideMenuList from '@/components/AsideMenuList'

export default {
  name: 'AsideMenu',
  components: { AsideTools, AsideMenuList },
  props: {
    menu: {
      type: Array,
      default: () => []
    }
  },
  computed: {
    ...mapState(['isAsideVisible'])
  },
  methods: {
    menuClick (item) {

    }
  }
}
</script>
