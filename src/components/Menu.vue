<template>
  <div class="menu">
    <link rel="stylesheet" href="http://code.ionicframework.com/ionicons/1.4.1/css/ionicons.min.css">
    <div class="top">
      <router-link to="/" class="menu__link" >
        <div class="main_icon">
          <img :src="icon" alt="icon" width="100%" height="100%">
        </div>
      </router-link>
    </div>
    <div class="menu__link">
      <p class="title">MyPortfolio!</p>
    </div>
    <div class="menu_items">
      <div class="works">
        <router-link to="/works" class="menu__link">Works</router-link>
      </div>
      <div class="contact">
        <router-link to="/contact" class="menu__link">Contact</router-link>
      </div>
      <div class="sns menu__link">      
        <span class="ion-social-twitter"></span>
        <span class="icon ion-social-github"></span>	
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return{
      icon: require('../assets/icon.png')
    };
  }
}
</script>
<style lang="scss" scoped>
$menuHeight: 100px;
.menu {
  border-bottom: solid 2px #8ccac1;
  background-color: #f1f1f1;
  height: $menuHeight;
  &__link {
    float: left;
    text-align: center;
    height: $menuHeight;
    line-height: $menuHeight;
    color: #18455a;
    width: $menuHeight;
    // border-right: 1px solid #f1f1f1;
    // border-left: 1px solid #f1f1f1;
    font-size: 30px;
      &:hover {
        background-color: #f1f1f1;
      }
    }
}
.menu_icon{
   float: left;
   width: 50%;
   height: 50%;
}
.menu{
  
}
.title{
  background-color:#f1f1f1 !important;
  padding: 0px;
  margin: 0px;
  font-size: 100%;
  width: 200%;
  color: #18455a;
}

.top{

}
.menu_items{
  display: flex;
  float: right;
}
.works{
  order: 1;
}
.contact{
  order: 2;
}
.sns{
  order: 3;
}
</style>
