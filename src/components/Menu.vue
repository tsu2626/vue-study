<template>
  <div class="menu">
    <link rel="stylesheet" href="http://code.ionicframework.com/ionicons/1.4.1/css/ionicons.min.css">
    <div class="top">
      <router-link to="/" class="menu__link" >
        <div class="main_icon">
          <img :src="icon" alt="icon" width="200px" height="200px">  
        </div>
      </router-link>
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
  background-color: #333;
  height: $menuHeight;
  &__link {
    float: left;
    text-align: center;
    height: $menuHeight;
    line-height: $menuHeight;
    color: white;
    width: 200px;
    border-right: 1px solid white;
    border-left: 1px solid white;
    font-size: 200%;
      &:hover {
        background-color: #444;
      }
    }
}
.menu_icon{
   float: left;
}
.menu{
  
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
