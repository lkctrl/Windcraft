<template>
  <!--菜单-->
  <Menu mode="horizontal" :theme="theme" active-name="1">
    <!--首页-->
    <MenuItem name="1" @click="gotoMainPage">首页</MenuItem>
    <!--介绍-->
    <MenuItem name="2">介绍</MenuItem>
    <!--截图-->
    <MenuItem name="3">截图</MenuItem>
    <!--op-->
    <MenuItem name="4">OP介绍</MenuItem>
    <!--历程-->
    <MenuItem name="5" @click="gotoCoursePage">历程</MenuItem>
    <!--op申请-->
    <MenuItem name="7">OP申请</MenuItem>
    <!--外挂举报-->
    <MenuItem name="8" @click="gotoReportPage">外挂举报</MenuItem>
    <!--成员动态-->
    <MenuItem name="9">成员动态</MenuItem>
    <!--小黑屋-->
    <MenuItem name="10" @click="gotoBanPage">封神榜</MenuItem>
    <!--消息-->
    <MenuItem name="11">公告</MenuItem>
    <!--搜索框连带搜索按钮-->
    <Input search enter-button style="width: auto" :border="false" placeholder="随便搜搜呗(≧∇≦)ﾉ"/>
  </Menu>
</template>

<script>
import router from "@/router";

export default{
  /**传参**/
  data () {
    return {
      //导航栏颜色
      theme: 'light',
    }
  },
  /**获取菜单栏选择项的id**/
  methods:{
    gotoCoursePage(){
      return router.push("/course")
    },
    gotoMainPage(){
      return router.push("/")
    },
    gotoBanPage(){
      return router.push("/ban")
    },
    gotoReportPage(){
      return router.push("/report")
    }
  }
}
</script>