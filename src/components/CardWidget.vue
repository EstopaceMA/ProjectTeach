<template>
  <card-component>
      <div class="level-item" style="background-color:#2D3E74; border-radius: 15px 15px 0 0; color:white; padding:0.2em;">
        {{label}}
      </div>
      <div class="level-item">

      </div>
  </card-component>
</template>

<script>
import CardComponent from '@/components/CardComponent'
export default {
  name: 'CardWidget',
  components: { CardComponent },
  props: {
    icon: {
      type: String,
      default: null
    },
    number: {
      type: Number,
      default: 0
    },
    prefix: {
      type: String,
      default: null
    },
    suffix: {
      type: String,
      default: null
    },
    label: {
      type: String,
      default: null
    },
    type: {
      type: String,
      default: null
    }
  }
}
</script>
