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
          class="tile is-child card-props complete-bg"
          label="2FN English Yr11"
        />
        <card-widget
          class="tile is-child card-props not-complete-bg"
          label="1LX Maths Yr10"
        />
        <card-widget
          class="tile is-child card-props complete-bg"
          label="English Year 8 1"
        />
        <card-widget
          class="tile is-child card-props not-complete-bg"
          label="NP Maths Year 10"
        />
        <card-widget
          class="tile is-child card-props not-complete-bg"
          label="NP Maths Year 10"
        />
        <card-widget
          class="tile is-child card-props complete-bg"
          label="2FN English Yr11"
        />
        <card-widget
          class="tile is-child card-props not-complete-bg"
          label="1LX Maths Yr10"
        />
        <card-widget
          class="tile is-child card-props complete-bg"
          label="English Year 8 1"
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

<style>
  .card-props{
    height: 18.2vw;
    border-radius: 15px;
  }
  .complete-bg {
    background-color: #e5e7f3;
  }

  .not-complete-bg{
    background-color: #f9f9f9;
  }
</style>

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
