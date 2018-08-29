<template>
  <div class="works">
    <div class="main">
      <div class="main__body">
        <ul class="works__list">
          <li v-for="(work, i) in works" class="works__item" @click="changeWork(i)">
            <h2>{{ work.title2 }}</h2>
          </li>
        </ul>
        <div class="contents">
          <div class="title_descri">
            <h1 class="main__title">{{ works[workIndex].title1 }}</h1>
            <p class="main__description">{{ works[workIndex].description }}</p>
          </div>
          <ul class="main__skillList">
            <li v-for="skill in works[workIndex].skills" class="main__skillItem">
              <img :src="require(`@/assets/${skill}`)">
            </li>
          </ul>
        </div>  
      </div>
    </div>   
  </div>
</template>
<script>
export default {
  data () {
    return {
      workIndex: 0,
      works: [
        {
          title1: 'EngineerSNS',
          title2: 'Work1',
          description: 'HTMLとCSSとJavaScript',
          skills: ['EngineerSNS.png']
        },
        {
          title1: '秘密の匿名掲示板',
          title2: 'Work2',
          description: 'HTMLとCSSとJavaScriptとjQueryを使って頑張った！',
          skills: ['html5.png', 'css3.png', 'javascript.png', 'jquery.png']
        },
        {
          title1: 'MyPortfolio!',
          title2: 'Work3',
          description: 'HTMLとCSSとSassとVueを使って頑張った！',
          skills: ['html5.png', 'css3.png', 'sass.png', 'vue.png']
        }
      ]
    }
  },
  methods: {
    changeWork (i){
      this.workIndex = i
    }
  }
}
</script>
<style lang="scss" scoped>
.main {
  // padding-bottom: 100px;
  margin-bottom: 30px;
  background-color: #fbf3f0 !important;
  &__body{
    // position: absolute;
    // top: 20%;
  }
  &__title {
    text-align: center;
    margin-top: 0px !important;
    margin-bottom: 0px;
  }
  &__description {
    margin: 0 auto 20px;
    width: 300px;
    text-align: center;
  }
  &__skill {
    &List {
      width:100%;
      display: flex;
      justify-content: center;
    }
    &Item {
      margin-left: 10%;
      position: relative;
      right: 10%;
      img {
        width: 80%;
        height: 80%;
        object-fit: contain;
      }
    }
  }
}
.main__title{
  padding-right: 50%;
  font-size: 300%;
  margin-top: 2%;
}
.main__description{
  padding-right: 45%;
  font-size: 150%;
}
// .title_descri{
//     padding-right: 55%;
// }
.works {
  &__list {
    margin: 0 auto;
    width: 500px;
    display: flex;
    justify-content: center;
    padding: 0;
    list-style: none;
    width: 0%;
    display: block;
    float: left;
    position: absolute;
    top: 30%;
    left: 5%;
  }
  &__item {
    border: 1px solid #fbf3f0;
    text-align: center;
    margin: 0 100%;
    width: 100%;
    height: 100%;
    line-height: 100%;
    vertical-align: middle;
    float: left;
    cursor: pointer;
    position: relative;
    left:50%;
    &:hover {
      background-color: #eee;
    }
  }
}
h2{
  color: #505050;/*文字色*/
  padding: 0.5em;/*文字周りの余白*/
  display: inline-block;/*おまじない*/
  line-height: 1.3;/*行高*/
  background: #8ccac1;/*背景色*/
  vertical-align: middle;/*上下中央*/
  border-radius: 25px 0px 0px 25px;/*左側の角を丸く*/
}

h2:before {
  content: '●';
  color: white;
  margin-right: 8px;
}
.contents{
  padding-top: 3%;
}
</style>
