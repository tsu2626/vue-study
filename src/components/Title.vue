<template>
  <div id="myPortfolio">
    <input type="button" @click="myPortfolio()" value="ホーム" style="display: none;">
  </div>
</template>
<script>
export default{
  data(){
    return{
      myPortfolio:require('../assets/MyPortfolio.png')
    };
  }
}
</script>

<style>

</style>
