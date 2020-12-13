<template>
<transition name="fade">
  <card-component v-if="isShow">
      <div class="level-item card-head">
        {{label}}
      </div>
      <div class="is-flex is-flex-direction-column" style="height: 89%">
        <div style="padding: 1em; height: 28%">
          <p style="font-size: 0.80rem; font-weight:bold;">STUDENTS COMPLETE: {{students_completed_count}} </p>
            <span>
              <p style="font-size: 0.80rem; font-weight:bold;">SELF-EVALUATION COMPLETE:
                <i v-if="is_self_eval_completed === true" class="mdi mdi-checkbox-marked-circle" style="color:#375096;"></i>
                <i v-else class="mdi mdi-close-circle" style="color:#C40024;"></i>
              </p>
            </span>
        </div>
        <div style="padding-left: 1em; padding-right: 1em; height: 0.5%">
          <hr>
        </div>
        <div v-if="is_self_eval_completed === true" class="is-flex is-justify-content-center is-align-items-center" style="height: 61.5%">
            <p style="font-weight: bold; font-size:0.80rem">SURVEY CLOSED</p>
        </div>
        <div v-else class="is-flex is-flex-direction-column" style="height: 61.5%">
          <div class="is-flex is-flex-direction-column is-justify-content-center" style="height:50%; padding:1em">
            <p style="font-size: 0.80rem;">
                <i class="mdi mdi-plus-circle" style="color:#375096;"></i>
                RUN STUDENT SURVEY
            </p>
            <p style="font-size: 0.80rem;">
                <i class="mdi mdi-plus-circle" style="color:#375096;"></i>
                COMPLETE SELF EVALUATION
            </p>
          </div>
          <div class="is-flex is-justify-content-center is-align-items-center" style="height:50%">
            <p style="font-weight: bold; font-size:0.85rem; cursor: pointer" @click="isShow = !isShow"> <i class="mdi mdi-close-box-outline"></i>  CLOSE SURVEY</p>
          </div>
        </div>
        <div class="is-flex is-justify-content-flex-end is-align-items-flex-end edit">
          <p style="cursor: pointer">EDIT</p>
        </div>
      </div>
  </card-component>
</transition>
</template>

<style>
  hr{
    margin: 0;
    background-color: #2d3e74;
    height: .5px;
  }
  .edit{
    height: 10%;
    font-size:0.75rem;
    padding-right: 10px;
    padding-bottom: 7px;
  }
  .card-head{
    background-color:#2D3E74;
    border-radius: 15px 15px 0 0;
    color:white; padding:0.2em;
    height: 11%;
  }

  .bounce-enter-active {
    animation: bounce-in .5s;
  }
  .bounce-leave-active {
    animation: bounce-in .5s reverse;
  }
  @keyframes bounce-in {
    0% {
      transform: scale(0);
    }
    50% {
      transform: scale(1.5);
    }
    100% {
      transform: scale(1);
    }
  }

  .fade-enter-active, .fade-leave-active {
    transition: opacity .5s;
  }
  .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
    opacity: 0;
  }
</style>

<script>
import CardComponent from '@/components/CardComponent'
export default {
  name: 'CardWidget',
  data: function () {
    return {
      isShow: true
    }
  },
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
    },
    students_completed_count: {
      type: String,
      default: '0'
    },
    is_self_eval_completed: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    remove: function () {
      this.isShow = false
    }
  }
}
</script>
