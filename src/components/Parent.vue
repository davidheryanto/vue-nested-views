<template>
  <div class="box">
    <h1 class="title is-5">Parent</h1>

    <div class="field">
      <div class="label">firstProp</div>
      <input class="input" v-model="firstProp"></input>
    </div>
    <div class="field">
      <div class="label">secondProp</div>
      <input class="input" v-model="secondProp"></input>
    </div>

    <i class="fa fa-lg fa-arrow-circle-down" aria-hidden="true"></i>
    <Child :firstPropFromParent="firstProp" :secondPropFromParent="secondProp"></Child>
  </div>
</template>

<script>

import Child from '@/components/Child'

export default {

  name: 'Parent',

  components: { Child },

  data () {
    return {
      firstProp: 'Parent default firstProp',
      secondProp: 'Parent default secondProp',
    };
  }
};
</script>

<style lang="css" scoped>


</style>
