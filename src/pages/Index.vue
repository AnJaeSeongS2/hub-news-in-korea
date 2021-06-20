<template>
  <h1>hello</h1>
</template>

<script>
const Parser = require('rss-parser');
const parser = new Parser();
const CORS_PROXY = 'https://cors-anywhere.herokuapp.com/';

export default {
  async created() {

    // https://github.com/rbren/rss-parser/issues/109 에 의해 require('http') 에 대한 이슈 대응.
    const response = await parser.parseURL(`${CORS_PROXY}https://bbs.ruliweb.com/best/humor/now?custom_list=best`)
    console.log(response)
    // naver news
    // const response = await this.$axios.get("https://cors-anywhere.herokuapp.com/https://news.naver.com/main/clusterArticles.nhn?id=c_202106081650_00000324&mode=LSD&mid=shm&sid1=100&oid=001&aid=0012446320")
    // google news (not working)
    // const response = await this.$axios.get("https://cors-anywhere.herokuapp.com/https://news.google.com/topstories?hl=ko&gl=KR&ceid=KR:ko")
    // const response = await this.$axios.get("https://cors-anywhere.herokuapp.com/https://lowell-dev.tistory.com/51")
  }
}
</script>

<style>

</style>