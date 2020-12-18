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
                    <form autocomplete="off">
                        <div class="content">
                            <p>When responding to the following questions and statements, please reflect on your classroom experiences with this teacher <strong>throughout the year.</strong></p>
                        </div>
                        <div>
                            <table>
                                <tr>
                                    <th></th>
                                    <th> Strongly disagree </th>
                                    <th>  </th>
                                    <th> Disagree </th>
                                    <th>  </th>
                                    <th> Neither agree nor disagree </th>
                                    <th>  </th>
                                    <th> Agree </th>
                                    <th>  </th>
                                    <th> Strongly agree </th>
                                </tr>
                                <tr class="row">
                                    <td><span>The teacher allowed us to pursue our own interests</span>
                                    <span class="icon has-text-danger" title="Please answer this question"><i class="fas fa-exclamation-circle"></i></span>
                                </td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="1"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="2"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="3"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="4"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="5"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="6"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="7"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="8"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="9"></label></td>
                                </tr>
                                <tr class="row">
                                    <td><span>Students were encouraged to openly express ideas</span>
                                    <span class="icon has-text-danger" title="Please answer this question"><i class="fas fa-exclamation-circle"></i></span>
                                </td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="1"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="2"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="3"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="4"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="5"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="6"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="7"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="8"></label></td>
                                <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="9"></label></td>
                                </tr>
                            </table>
                        </div>
                    </form>
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                </b-step-item>

                <b-step-item icon="chart-bar" :clickable="isStepsClickable">
                    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                </b-step-item>

                <b-step-item icon="flag" label="Finish" :clickable="isStepsClickable" disabled>
                    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                </b-step-item>

                <template
                    v-if="customNavigation"
                    slot="navigation"
                    slot-scope="{next}">
                    <b-button
                        outlined
                        type="is-info"
                        :disabled="next.disabled"
                        @click.prevent="next.action"
                        style="margin-left: 1vw">
                        Next
                    </b-button>
                </template>
            </b-steps>
        </section>
    </div>
</template>

<style scoped>
    th {
        background-color: #fff;
    }

    td{
        border-top: 1px solid #dbdbdb;
        border-bottom: 1px solid #dbdbdb;
    }

    section {
        background-color: #fff;
    }
</style>

<script>
export default {
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
      mobileMode: 'minimalist'
    }
  }
}
</script>
