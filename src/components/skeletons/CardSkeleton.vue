<template>
  <div class="row q-ma-sm q-col-gutter-sm">
      <div class="col-4" v-for="c in cards"
          :key="c">
        <q-card style="height: 534px">
          <q-skeleton height="200px" square />
          <q-item v-for="l in linhas" :key="l">
            <q-item-section>
              <q-item-label>
                <q-skeleton type="text" />
              </q-item-label>
            </q-item-section>
          </q-item>

        </q-card>
      </div>
    </div>
</template>

<script>
export default {
  name: 'TableSkeleton',
  props: {
    cards: {
      type: Number,
      default: 3,
      required: false
    },
    linhas: {
      type: Number,
      default: 3,
      required: false
    }
  }
}
</script>
