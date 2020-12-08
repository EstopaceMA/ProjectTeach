<template>
  <div>
    <!-- <title-bar :title-stack="titleStack" /> -->
    <home-head :has-right-visible="true">
      St. Patricks Public School <br>
      <p style="font-size:0.5em">Survey Period: 23 June to 30 August 2020</p>
      <template #right>
          <button class="button is-link is-rounded">
              <span>ADD CLASS SURVEY</span>
              <span class="icon">
                <i class="mdi mdi-plus-circle" style="color:#fff;"></i>
              </span>
          </button>
      </template>
    </home-head>
    <section class="section is-main-section">
      <tiles>
        <card-widget
          class="tile is-child"
          type="is-primary"
          icon="account-multiple"
          :number="512"
          label="Clients"
        />
        <card-widget
          class="tile is-child"
          type="is-info"
          icon="cart-outline"
          :number="7770"
          prefix="$"
          label="Sales"
        />
        <card-widget
          class="tile is-child"
          type="is-success"
          icon="chart-timeline-variant"
          :number="256"
          suffix="%"
          label="Performance"
        />
      </tiles>

      <!-- <card-component title="Clients" class="has-table has-mobile-sort-spaced">
        <clients-table-sample
          :data-url="`${$router.options.base}data-sources/clients.json`"
        />
      </card-component> -->
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Tiles from '@/components/Tiles'
import CardWidget from '@/components/CardWidget'
import HomeHead from '@/components/HomeHead'
export default {
  name: 'Home',
  components: {
    CardWidget,
    Tiles,
    HomeHead
  }
}
</script>
