<template>
  <transition name="fade">
    <div class="article">
      <article>
        <h1 v-cloak>{{filteredData.title}}</h1>
        <h3 v-cloak class="mt-5 mb-4"><a :href="filteredData.url" target="_blank">{{ filteredData.urlTitle}}</a></h3>
        <div v-for="p in filteredData.picture" v-if="p.id==='1'" class="mb-5">
          <img :src="p.path" class="picture">
        </div>
        <div class="workdetail">
          <div class="yearroll">
            <p v-cloak class="year"><span>制作:</span>　{{ filteredData.year }}</p>
            <p v-cloak class="roll"><span>my role:</span>　{{ filteredData.role }}</p>
          </div>
          <p v-cloak class="descriptiontext">{{ filteredData.text }}</p>
          <!-- <p v-cloak><a :href="filteredData.url" target="_blank">{{ filteredData.urlTitle}}</a></p> -->
          <div v-for="p in filteredData.picture" v-if="p.id !== '1'">
            <img :src="p.path">
          </div>
        </div>
      </article>
    </div>
  </transition>
</template>

<script>
export default{
  title:'....',
  description:'....',
  props:['data'],
  mounted(){
    document.title = this.filteredData.title + '- Tomoro\'s Portfolio'

    let meta =document.getElementByTagName('meta')
    for(var i = 0; i<meta.length; i++){
      if (meta[i].name.toLowerCase()=='description'){
        meta[i].content = 'Tomoroが作成した'+this.filteredData.title+'のページです'
      }
    }
  },
  computed:{
    filteredData:function(){
      var url=window.location.protocol+'//'+window.location.host+'/works/'
      var matchData=this.data.filter(function(item,index){
        if (item.slug === window.location.href.replace(url,'')) return true;
      })
      return matchData[0]
    }
  }
}
</script>

<style>
span{
  /* font-size: 15px; */
  color: #6b6d6d;
}

.workdetail{
  width:40%;
  margin-left: auto;
  margin-right: auto;
}

.picture{
  width:400px;
  height: 210px;
}

.descriptiontext, .yearroll{
  width:400px;
  margin-left: auto;
  margin-right: auto;
}

/* .yearroll{
  width:400px;
} */

.yearroll p{
  font-size: 13px;
}

.year{
  float:left;
  width:200px;
}

.roll{
  float:right;
  width:200px;
}

@media (max-width:770px){
  .workdetail{
    width:40%;
    margin-left: auto;
    margin-right: auto;
  }

  .picture{
    width:300px;
    height: 180px;
  }

  .descriptiontext, .yearroll{
    width:300px;
    margin-left: auto;
    margin-right: auto;
  }

  .yearroll p{
    font-size: 13px;
  }

  .year{
    float:left;
    width:150px;
  }

  .roll{
    float:right;
    width:150px;
  }

  .workdetail{
    width:300px;
    margin-left: auto;
    margin-right: auto;
  }

}




</style>
