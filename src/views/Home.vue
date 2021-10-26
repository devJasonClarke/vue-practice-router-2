<template>
  <div>
<h1>Counter</h1>
<h2 class="state">{{state}}</h2>
<Count :lee='state'>
<button class="add" @click="add">+ add</button>
<button class="minus" @click="minus"> - minus</button>
</Count>

<button class="add" @click="ma"> Go To Ma</button>
  </div>
</template>

<script>
import Count from '@/components/count';
  export default {
    components: {
     Count,
    },
    data() {
      return {
        state: 0
      }
    },
    methods: {
      add() {
        this.state++;
      },
      minus() {
        this.state--;
      },
      ma(){
       this.$router.push({path: 'Ma'})
      }
    },
  }
</script>

<style lang="scss" scoped>

</style>