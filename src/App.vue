<template>
  <div class="tile is-ancestor" style="margin-top: 0.75rem; margin-left: 0.65rem;">
    <div class="tile is-parent is-6">
      <article class="tile is-child box">
        <h1 class="title">Demo</h1>
        <div class="block">
          <p>
            <slider type="success" size="large" :value="value" :max="100" :step="1" is-fullwidth></slider>
          </p>
          <p>
            <input class="input" type="number" v-model="value" min="0" max="100" number>
          </p>
        </div>
      </article>
    </div>
  </div>
</template>

<script>
import Slider from 'vue-bulma-slider'

export default {
  components: {
    Slider
  },

  data () {
    return {
      value: 23
    }
  },

  computed: {
    per () {
      return this.value + '%'
    }
  },

  methods: {
    update (val) {
      this.value = Number(val)
    }
  }

 }
</script>

<style lang="scss">
@import '~bulma';

p {
  margin-bottom: 20px;
}
</style>