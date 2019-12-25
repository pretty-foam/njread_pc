<template>
  <div id="app" >
          <nav class="" ref="nav"> 
              <div class="nav_content">
                    <img src='./assets/home_logo.png' alt="牛角阅读">
              </div>
          </nav>
          <div class="banner" ref="banner">
                <div class="banner_content">
                      <div class="left">
                          <img src="./assets/home_img1.png"   width="550" height="624" >
                      </div>
                      <div class="right">
                          <div class="title">
                              <h1>海量小说</h1>
                              <h1>免费小说</h1>
                          </div>
                          <div class="QRcode">
                            <img src="./assets/home_one_code.png" alt="" width="240" height="240">
                          </div>  
                      </div>
                </div>
          </div>
          <div class="cell">
               <div class="cell_content">
                    <div class="left">
                          <div class="title">海量小说</div>
                          <p>男频女频十万本热门小说，通通免费！全职高手、赘婿、牧神记、斗破苍穹、全球高武，琅琊榜、好想住你隔壁、重生十六岁、天芳、女帝直播攻略，永久免费！</p>
                    </div>
                    <div class="right">
                          <img src="./assets/home_img2.png" alt="" width="500" height="700">
                    </div>
               </div>
          </div>
          <div class="cell">
            <div class="cell_content">
                 <div class="left">
                      <div class="title">丰富书城</div>
                      <p>精选、男生、女生、图书四大版块，重磅推荐、人气小说两大分区，小编为你精心推荐。在这里，能读到的不止是免费。</p>
                </div>
                <div class="right">
                      <img src="./assets/home_img3.png" alt="">
                </div>
            </div>
          </div>
          <div class="footer">
               <div class="container">
                      <div class="footer-left">
                          <p>上海寅诚网络科技有限公司</p>
                          <p>上海市浦东新区盛夏路560号306室</p>
                          <p><a href="http://www.beian.miit.gov.cn">沪ICP备19024884号-1</a></p>
                      </div>
                      <div class="footer-right">
                            <img src="./assets/home_bottom_code.png" alt="" width="198" height="198">
                      </div>
               </div>
          </div>
  </div>
</template>
<script>
export default {
  data(){
    return{
       pic:'./home_logo.png'
    }
  },
  methods:{
    init(){
        window.document.addEventListener('scroll',(e)=>{
           const nav = this.$refs.nav
           const top = this.$refs.banner.getBoundingClientRect().top 
           top <100 ? nav.className ='nav--shadow' :nav.className =''
        })
    }
  },
  mounted(){
    this.init()
  }
}
</script>

<style lang="stylus" scoped>
#app 
  nav 
    width 100%
    height 100px
    background white
    position fixed
    top 0
    left 0
    .nav_content
      width 1200px
      height 100%
      display flex
      align-items center
      margin auto 
  .nav--shadow
    box-shadow 0px 8px 10px rgba(0, 0, 0, 0.1)
  .banner
    background rgba(255, 240, 225, 1)
    margin-top 100px
    padding 100px 0 0 0
    .banner_content
      width 1200px
      margin auto 
      display flex
      justify-content space-between
      .left> img 
          vertical-align top
      .right
        display flex
        justify-content center
        align-items center
        flex-flow column nowrap
        margin-right 105px
        font-size 30px
        font-weight 600
        h1 
          margin-bottom 20px
        h1:nth-child(2)
          color  RGBA(254, 92, 67, 1)
  .cell
    background #eff3f7
    padding-top 100px
    .cell_content
      width 1200px
      margin auto 
      display flex
      justify-content space-between
      flex-flow row nowrap
      .title
        color  rgba(51, 51, 51, 1)
        font-size 60px
        font-weight 600
        margin-top 80px
      p 
        color rgba(102, 102, 102, 1)
        font-size 30px 
        line-height 50px
        width 500px
        margin-top 40px
  .cell:nth-child(4)
    background rgba(255, 255, 255, 1)
    .cell_content 
      flex-flow row-reverse nowrap
  .footer
    background rgba(247, 251, 255, 1)
    padding 80px 0
    .container 
      width 1200px
      display flex
      margin auto 
      justify-content space-between
      p 
        margin auto 
        font-size 30px
        color RGBA(51, 51, 51, 1)
        line-height 60px
      p:nth-child(1)
        color  rgba(51, 51, 51, 1)
        font-weight 600
      a 
        color  rgba(51, 51, 51, 1)
        text-decoration none
</style>
