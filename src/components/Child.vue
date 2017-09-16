<template>
  <div class="box">
    <h1 class="title is-5">Child</h1>

    <div class="field">
      <div class="label">firstProp</div>
      <input class="input" v-model="firstProp"></input>
    </div>
    <div class="field">
      <div class="label">secondProp</div>
      <input class="input" v-model="secondProp"></input>
    </div>
    <div class="field">
      <div class="label">thirdProp</div>
      <input class="input" v-model="thirdProp"></input>
    </div>

    <i class="fa fa-lg fa-arrow-circle-down" aria-hidden="true"></i>
    <GrandChild :secondPropFromParent="secondProp" :thirdPropFromParent="thirdProp"></GrandChild>
  </div>
</template>

<script>

import GrandChild from '@/components/GrandChild'


export default {

  name: 'Child',

  components: { GrandChild },

  props: [ 'firstPropFromParent', 'secondPropFromParent' ],

  data () {
    return {
      firstProp: 'Child default firstProp',
      secondProp: 'Child default secondProp',
      thirdProp: 'Child default thirdProp',
    };
  },

  watch: {
    firstPropFromParent(val) {
      this.firstProp = val
    },
    secondPropFromParent(val) {
      this.secondProp = val
    },
  },

};
</script>

<style lang="css" scoped>
</style>
