<template>
  <section class="hero is-hero-bar">
    <div class="hero-body hero-body-prop">
      <div class="level">
        <div class="level-left">
          <div class="level-item">
            <h1 class="title">
              <slot />
            </h1>
          </div>
        </div>
        <div v-show="hasRightVisible" class="level-right">
          <div class="level-item">
            <slot name="right" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
  .hero-body-prop{
    padding: 2rem 8vw 1rem 8vw !important;
  }
</style>

<script>
export default {
  name: 'HomeHead',
  props: {
    hasRightVisible: {
      type: Boolean,
      default: true
    }
  }
}
</script>
