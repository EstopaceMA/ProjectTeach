<template>
    <div>
        <section style="padding: 5vw">
            <b-steps
                v-model="activeStep"
                :animated="isAnimated"
                :rounded="isRounded"
                :has-navigation="hasNavigation"
                :icon-prev="prevIcon"
                :icon-next="nextIcon"
                :label-position="labelPosition"
                :mobile-mode="mobileMode"
                type="is-info">
                <b-step-item icon="play" label="Start" :clickable="isStepsClickable">
                    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    <div class="content">
                        <p>When responding to the following questions and statements, please reflect on your classroom experiences with this teacher <strong>throughout the year.</strong></p>
                    </div>
                    <div>
                        <survey-table></survey-table>
                    </div>
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    <div class="content">
                        <p>When responding to the following questions and statements, please reflect on your classroom experiences with this teacher <strong>throughout the year.</strong></p>
                    </div>
                    <div>
                        <survey-table></survey-table>
                    </div>
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    <div class="content">
                        <p>When responding to the following questions and statements, please reflect on your classroom experiences with this teacher <strong>throughout the year.</strong></p>
                    </div>
                    <div>
                        <survey-table></survey-table>
                    </div>
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    <div class="content">
                        <p>When responding to the following questions and statements, please reflect on your classroom experiences with this teacher <strong>throughout the year.</strong></p>
                    </div>
                    <div>
                        <survey-table></survey-table>
                    </div>
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    <div class="content">
                        <p>When responding to the following questions and statements, please reflect on your classroom experiences with this teacher <strong>throughout the year.</strong></p>
                    </div>
                    <div>
                        <survey-table></survey-table>
                    </div>
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    <div class="content">
                        <p>When responding to the following questions and statements, please reflect on your classroom experiences with this teacher <strong>throughout the year.</strong></p>
                    </div>
                    <div>
                        <survey-table></survey-table>
                    </div>
                </b-step-item>

                <b-step-item icon="flag" label="Finish" :clickable="isStepsClickable" disabled>
                    <div class="content">
                        <p>When responding to the following questions and statements, please reflect on your classroom experiences with this teacher <strong>throughout the year.</strong></p>
                    </div>
                    <div>
                        <survey-table></survey-table>
                    </div>
                </b-step-item>
                <template
                    v-if="customNavigation"
                    slot="navigation"
                    slot-scope="{previous, next}">
                    <div class="button-container">
                        <b-button
                            outlined
                            type="is-info"
                            @click.prevent="previous.action"
                            @click="backBtn"
                            style="margin-left: 1vw">
                            Back
                        </b-button>
                        <b-button
                            outlined
                            type="is-info"
                            @click.prevent="next.action"
                            @click="nextBtn"
                            style="margin-right: 1vw">
                            Next
                        </b-button>
                    </div>
                </template>
            </b-steps>
            <b-progress class="progress" :value="progress" size="is-small" format="percent"></b-progress>
        </section>
    </div>
</template>

<style scoped>
    section {
        background-color: #fff;
    }

    .progress {
        width: 30%;
        margin: auto;
        margin-top: 50px;
    }

    .button-container {
        display: flex;
        justify-content: space-between;
    }

    nav {
        display: none;
    }
</style>
<style>
    .b-steps nav {
        display: none;
    }
</style>

<script>
import SurveyTable from '../components/SurveyTable.vue'
export default {
  components: { SurveyTable },
  name: 'Steps',
  data () {
    return {
      activeStep: 0,

      showSocial: false,
      isAnimated: true,
      isRounded: true,
      isStepsClickable: false,

      hasNavigation: true,
      customNavigation: true,
      isProfileSuccess: false,

      prevIcon: 'chevron-left',
      nextIcon: 'chevron-right',
      labelPosition: 'bottom',
      mobileMode: 'minimalist',
      progress: 0
    }
  },
  methods: {
    nextBtn () {
      if (this.progress !== 105) {
        this.progress = this.progress + 15
      }
    },

    backBtn () {
      if (this.progress !== 0) {
        this.progress = this.progress - 15
      }
    }
  }
}
</script>
