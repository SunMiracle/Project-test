<template>
  <div id="App">
  	<div class="AppHeader">
    	<div class="AppHeaderImage">
        <!-- 敲重点 图片会被WebPack 转化为字符串 如果需要使用Vue来进行赋值， 需要使用require -->
        <img :src="headerImage">
      </div>
      <div class="AppHeaderTab">
        <ul class="AppHeaderTabBox">
            <li v-for="todo in headerTab">{{todo.text}}</li>
        </ul>
      </div>
  	</div>
    <!-- 当前路由所显示的内容 -->
    <router-view/>
  </div>
</template>
<script>
  
export default {
  name: 'App',
  data(){
    return{
      headerImage: require('./assets/logo_mtop.png'),
      headerTab:[
        {
          text: '首页',
          link: '/'
        },
        {
          text: '新闻中心',
          link: '/news'
        },
        {
          text: '校园招聘',
          link: 'Recruiting'
        },
        {
          text: '关于多益',
          link: 'about'
        }
      ]
    }
  }
}
function s(){
  return 0;
}
</script>

<style>
body {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0px;
}
body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,textarea,p,blockquote,th,td,hr,button,article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section {
    margin:0;
    padding:0;
}
.AppHeader{
  text-align: center;
}
.AppHeaderImage{ 
  padding: 8px 0px;
  text-align: center;
  background: black;
}
.AppHeaderImage img{
  width: 200px; 
}
.AppHeaderTab{
  background: #26292b;
  padding: 15px 8px;
  color: white;
}
.AppHeaderTabBox{
  list-style: none;
  display: flex;
  font-size: 1.35em;
  justify-content: space-between;
  font-weight: bold;
}
@media screen and (max-width: 350px) {
  .AppHeaderTabBox{
    font-size: 1.2em;
  }
}
</style>
