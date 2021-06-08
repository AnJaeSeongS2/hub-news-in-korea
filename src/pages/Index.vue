<template>
  <h1>hello</h1>
</template>

<script>
export default {
  async created() {
  const response = await this.$axios.get("https://cors-anywhere.herokuapp.com/https://bbs.ruliweb.com/best/humor/now?custom_list=best")
    // naver news
    // const response = await this.$axios.get("https://cors-anywhere.herokuapp.com/https://news.naver.com/main/clusterArticles.nhn?id=c_202106081650_00000324&mode=LSD&mid=shm&sid1=100&oid=001&aid=0012446320")
    // google news (not working)
    // const response = await this.$axios.get("https://cors-anywhere.herokuapp.com/https://news.google.com/topstories?hl=ko&gl=KR&ceid=KR:ko")
    // const response = await this.$axios.get("https://cors-anywhere.herokuapp.com/https://lowell-dev.tistory.com/51")
    console.log(response.data)
  }
}
</script>

<style>

</style>