<template>
  <footer v-show="isFooterBarVisible" class="footer">
    <div class="container-fluid">
      <div class="level">
        <div class="level-left">
          <div class="level-item">
            <div class="footer-copyright">
              <b>&copy; {{ year }}</b> &mdash; Teach
              <span class="tag">v1.0.0</span>
            </div>
            <div class="footer-copyright">
              <a href="#">Privacy Policy</a>
            </div>
          </div>
        </div>
        <div class="level-right">
          <div class="level-item">
            <div class="logo">
              <a href="#">
                <img style="height: 90px" src="../assets/teach_logo.png" alt="teach_logo" />
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import dayjs from 'dayjs'
import { mapState } from 'vuex'

export default {
  name: 'FooterBar',
  computed: {
    year () {
      return dayjs().year()
    },
    ...mapState(['isFooterBarVisible'])
  }
}
</script>
