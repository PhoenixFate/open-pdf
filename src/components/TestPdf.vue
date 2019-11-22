<template>
  <div class="test">
    <iframe class="prism-player" :src="pdfUrl" width="100%" height="100%"></iframe>
  </div>
</template>

<script>

    export default {
        name: "TestPdf",

        data(){
          return {
            pdfUrl:''
          }
        },

        created() {
          console.log("create test pdf")
          // 这儿的url， 就是通过 axios 进行请求的地址，只不过换成了从导航url进行请求的方式

          let url = 'https://jbtest.njzhyl.cn/picture/test2.pdf'

          let url2 = 'b.pdf'
          this.pdfUrl = './static/web/viewer.html?file='+encodeURIComponent(url2)
        }
    }
</script>

<style scoped>
  page,body,html {
    height: 100%;
  }

  .test {
    height: 100%;
    width: 100%;
  }
</style>
