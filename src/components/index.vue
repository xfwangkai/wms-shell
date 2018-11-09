<template>
  <mu-container>
    <mu-text-field label="请输入IP地址" v-model="ipaddr"></mu-text-field>
    <mu-button @click="openNewPage">打开新链接</mu-button>
  </mu-container>
</template>

<script>
    export default {
      name: "index",
      data() {
        return {
          ipaddr: ''
        }
      },
      methods: {
        openNewPage() {
          window.location.href = `http://${this.ipaddr}:8088`
        }
      }
    }
</script>

<style scoped>

</style>
