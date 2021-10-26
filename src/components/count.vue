<template>
  <div>
    {{lee}}
    {{g}}
    get therm
<slot></slot>
  </div>
</template>

<script>
  export default {
    name: "Count",
    props: {
      lee: {
        type: Number,
        default: 0
      },
    },
    data() {
      return {
        g: 0
      }
    },
    methods: {
      add() {
   this.$emit('add');
      }
    },
  }
</script>

<style lang="scss" >
button{
  outline: none;
  border: none;
  border-radius: 10px;
  padding: 10px 20px;
cursor: pointer;
  margin-right: 15px;
transition: .3s all ease-in-out;
  &:hover{
    transform: scale(1.1);
  }
}
.add{
  background-color: dodgerblue;
}
.minus{
  background-color: orange;
}

</style>