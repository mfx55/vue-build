<template>
  <div class="index">
    <div class="title" @click='linkToRank'>{{msg}}</div>
  </div>
</template>

<script>
export default {
   metaInfo: {
    title: '首页', // set a title
    meta: [{
      name: 'renderer',
      content: 'webkit'
    }],
    link: [{                 // set link
      rel: 'asstes',
      href: 'https://assets-cdn.github.com/'
    }]
  },
  data () {
    return {
      msg: 'ASO100 index'
    }
  },
  methods: {
    linkToRank() {
       this.$router.push({name: 'rank', params: { appid: 123,country: 'cn'}});
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  
@import './../assets/css/common.scss';

.index{
  .title{
    font-size: 24px;
    color: #abcdef;
  }
  .content{
    font-size: 26px;
    @include dot(200px)
  }
}
  
</style>
