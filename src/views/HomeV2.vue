<template>
  <div>
    <!-- <title-bar :title-stack="titleStack" /> -->
    <home-head :has-right-visible="true">
      St. Patricks Public School <br>
      <p style="font-size:0.5em; color: #395297">Survey Period: 23 June to 30 August 2020</p>
      <template #right>
          <button class="button is-link is-rounded" style="background-color: #395297">
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
          class="tile is-child card-props complete-bg complete"
          label="2FN English Yr11"
          students_completed_count="14"
          is_self_eval_completed
        />
        <card-widget
          class="tile is-child card-props not-complete-bg"
          label="1LX Maths Yr10"
        />
        <card-widget
          class="tile is-child card-props complete-bg complete"
          label="English Year 8 1"
          students_completed_count="14"
          is_self_eval_completed
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
          class="tile is-child card-props complete-bg complete"
          label="2FN English Yr11"
          students_completed_count="14"
          is_self_eval_completed
        />
        <card-widget
          class="tile is-child card-props not-complete-bg"
          label="1LX Maths Yr10"
        />
        <card-widget
          class="tile is-child card-props complete-bg complete"
          label="English Year 8 1"
          students_completed_count="14"
          is_self_eval_completed
        />
      </tiles>

      <!-- <card-component title="Clients" class="has-table has-mobile-sort-spaced">
        <clients-table-sample
          :data-url="`${$router.options.base}data-sources/clients.json`"
        />
      </card-component> -->
    </section>
    <section>
      <hero-bar style="background-color: #f8f8f8; padding-left: 8vw; padding-right: 8vw">
        Past Results
      </hero-bar>
      <clients-table-sample style="background-color: #fff; padding-left: 8vw; padding-right: 8vw; padding-top: 4vw;"
          :data-url="`${$router.options.base}data-sources/past_results.json`"
          :checkable="false"
        />
    </section>
  </div>
</template>

<style>
  .card-props{
    border-radius: 15px;
    border: solid 1px #2e3f75;
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
import HeroBar from '@/components/HeroBar'
import ClientsTableSample from '@/components/ClientsTableSample'
export default {
  name: 'Home',
  components: {
    CardWidget,
    Tiles,
    HomeHead,
    HeroBar,
    ClientsTableSample
  }
}
</script>
