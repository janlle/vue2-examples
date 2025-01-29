<template>
  <div class="person">
    <h2>当前求和：{{ sum }}</h2>
    <button @click="add">加法</button>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Person',
  data() {
    return {
      sum: 1
    }
  },
  methods: {
    add() {
      this.sum += 1
      console.log("sum")
    },
  },
  beforeCreate() {
    console.log("创建前")
  },
  created() {
    console.log('创建完毕')
  },
  beforeMount() {
    console.log("挂载前")
  },
  mounted() {
    console.log('挂载完毕')
  },
  beforeUpdate() {
    console.log('更新前')
  },
  updated() {
    console.log('更新完毕')
  },
  beforeDestroy() {
    console.log('销毁前')
  },
  destroyed() {
    console.log('销毁后')
  }
}
</script>

<style scoped>
.person {
  background-color: #ddd;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
</style>
