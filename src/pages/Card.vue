<template>
  <q-page>
    <div class="row q-ma-sm q-col-gutter-sm" v-if="load">
        <div class="col-4" v-for="c in 6"
          :key="c">
          <q-card>
            <img src="https://cdn.quasar.dev/img/mountains.jpg">
            <q-card-section>
              <div class="text-h6">Our Changing Planet</div>
              <div class="text-subtitle2">by John Doe</div>
            </q-card-section>
            <q-card-section class="q-pt-none">
              {{ lorem }}
            </q-card-section>
          </q-card>
        </div>
    </div>

    <card-skeleton
      v-else
      :cards="6"
      :linhas="5"
    />

  </q-page>
</template>

<script>
import CardSkeleton from 'components/skeletons/CardSkeleton.vue'

export default {
  name: 'Card',
  components: { CardSkeleton },
  data () {
    return {
      load: false,
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
    }
  },
  mounted () {
    setTimeout(() => {
      this.load = true
    }, 5000)
  }
}
</script>
