<template>
  <div class="box">
    <h1 class="title is-5">GrandChild</h1>

    <div class="field">
      <div class="label">secondProp</div>
      <input class="input" v-model="secondProp"></input>
    </div>
    <div class="field">
      <div class="label">thirdProp</div>
      <input class="input" v-model="thirdProp"></input>
    </div>

  </div>
</template>

<script>
export default {

  name: 'GrandChild',

  props: [ 'secondPropFromParent', 'thirdPropFromParent',  ],

  watch: {
    secondPropFromParent(val) {
      this.secondProp = val
    },
    thirdPropFromParent(val) {
      this.thirdProp = val
    },
  },

  data () {
    return {
      secondProp: 'GrandChild default secondProp',
      thirdProp: 'GrandChild default thirdProp',
    };
  }
};
</script>

<style lang="css" scoped>
</style>
