<template>
  <h1>hello</h1>
</template>

<script>
export default {
  async created() {
    const response = await this.$axios.get("https://cors-anywhere.herokuapp.com/https://news.google.com/topstories?hl=ko&gl=KR&ceid=KR:ko")
    console.log(response.data)
  }
}
</script>

<style>

</style>