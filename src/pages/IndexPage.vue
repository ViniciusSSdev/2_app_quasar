<template>
  <q-page class="flex flex-center" style="flex-direction: column ;" >
      <q-circular-progress
      indeterminate
      size="100px"
      :thickness="0.4"
      font-size="50px"
      color="lime"
      track-color="grey-3"
      center-color="grey-8"
      class="q-ma-md"
    />

    <q-btn class="flex flex-center" style="margin-top: 95px;" label="Clique Aqui" color="primary" @click="persistent = true" />

    <q-dialog v-model="persistent" persistent transition-show="scale" transition-hide="scale">
      <q-card class="bg-teal text-white" style="width: 300px">
        <q-card-section>
          <div class="text-h6">Site ainda não finalizado, muito apressado!</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
        </q-card-section>

        <q-card-actions align="right" class="bg-white text-teal">
          <q-btn flat label="OK" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>

    <img
    class="flex flex-direction"
      alt="Quasar logo"
      src="~assets/cst.png"
      style="width: 400px; height: auto; margin: 35px;"
    >
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import { ref } from 'vue'


export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
    value: 71,
     persistent: ref(false)
    }
  },
})
</script>
