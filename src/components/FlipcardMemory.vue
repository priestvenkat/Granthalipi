<template>
  <vue-flip :active-click="true" width="140px" height="120px" transition="2s" class="q-ma-sm flip cursor-pointer">
        <div slot="front">
          <q-card inline class="cards" color="tertiary">
            <q-card-main>
            </q-card-main>
          </q-card>
        </div>
        <div slot="back">
          <q-card inline class="cards">
            <q-card-main align="center">
              <font size="6" class="sharada">{{convertDS(text)}}</font>
            </q-card-main>
          </q-card>
        </div>
  </vue-flip>
</template>

<script>
import VueFlip from 'vue-flip'
import {QCard, QCardTitle, QCardMain, QCardMedia, QCardActions} from 'quasar'
import { ScriptMixin } from '../mixins/ScriptMixin'

export default {
  // name: 'ComponentName',
  props: ['text', 'script'],
  mixins: [ScriptMixin],
  components: {
    VueFlip,
    QCard,
    QCardTitle,
    QCardMain,
    QCardMedia,
    QCardActions
  },
  data () {
    return {}
  }
}
</script>

<style scoped>
.cards {
  width:140px;
  height:120px;
}
.flip {
  display: inline-block;
}
</style>
