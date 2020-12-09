<template>
  <card-component>
      <div class="level-item" style="background-color:#2D3E74; border-radius: 15px 15px 0 0; color:white; padding:0.2em;">
        {{label}}
      </div>
      <div style="padding: 1em">
        <p style="font-size: 0.80rem; font-weight:bold;">STUDENTS COMPLETE: {{students_completed_count}} </p>
          <span>
            <p style="font-size: 0.80rem; font-weight:bold;">SELF-EVALUATION COMPLETE:
              <i v-if="is_self_eval_completed === true" class="mdi mdi-checkbox-marked-circle" style="color:#375096;"></i>
              <i v-else class="mdi mdi-close-circle" style="color:#C40024;"></i>
            </p>
          </span>
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
    },
    students_completed_count: {
      type: String,
      default: '0'
    },
    is_self_eval_completed: {
      type: Boolean,
      default: false
    }
  }
}
</script>
