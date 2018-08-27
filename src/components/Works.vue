<template>
  <div class="works">
    <div class="main">
      <ul class="works__list">
        <li v-for="(work, i) in works" class="works__item" @click="changeWork(i)">
          <h2>{{ work.title2 }}</h2>
        </li>
      </ul>
      <h1 class="main__title">{{ works[workIndex].title1 }}</h1>
      <p class="main__description">{{ works[workIndex].description }}</p>
      <ul class="main__skillList">
        <li v-for="skill in works[workIndex].skills" class="main__skillItem">
          <img :src="require(`@/assets/${skill}`)">
        </li>
      </ul>     
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
  background-color: #fbf3f0;
  border-bottom: 1px solid #ddd;
  margin-bottom: 30px;
  &__title {
    text-align: center;
    margin-top: 0px !important;
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
      img {
        width: 100%;
        height: 100%;
        object-fit: contain;
      }
    }
  }
}
.main__title{
  padding-right: 65%;
  font-size: 300%;
  margin-top: 2%;
}
.main__description{
  padding-right: 60%;
  font-size: 150%;
}
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
    top: 50%;
    left: 5%;
  }
  &__item {
    border: 1px solid #ddd;
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
</style>
