<template>
  <div>
    <hero-bar>
      Profile
    </hero-bar>
  </div>
</template>

<script>
import { mapState } from 'vuex'
import HeroBar from '@/components/HeroBar'
export default {
  name: 'Profile',
  components: {
    HeroBar
  },
  computed: {
    titleStack () {
      return ['Admin', 'Profile']
    },
    ...mapState(['userName', 'userEmail'])
  }
}
</script>
