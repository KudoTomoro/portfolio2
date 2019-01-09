<template>
  <div class="top">
    <h1>
      {{ msg }}
    </h1>
  </div>
</template>

<script>
export default {
  name: 'top',
  title:'Top',
  description:'Tomoroのポートフォリオサイト',
  data () {
    return {
      msg: 'Welcome to Tomoro\'s portfolio'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.top{
  display: block;
  left: 0;
  right: 0;
  margin-top:0;
  height: 100vh;
  background: linear-gradient(to right, #01CCD3, #A3FEC3);
}

.top h1{
  /* height: 100vh; */
  line-height: 600px;
  /* vertical-align: middle; */
  background: linear-gradient(to right, #01CCD3, #A3FEC3);
}

@media (max-width:380px){
  .top{
    /* height: 500px; */
    /* background: linear-gradient(to right, #01CCD3, #A3FEC3); */
    height: 95vh;
  }

  .top h1{
    font-size: 17px;
    line-height: 625px;
  }
}

@media screen and (min-width:768px) and ( max-width:1024px){
  .top{
    /* height: 9150px; */
  }

  .top h1{
    font-size:20px;
    line-height: 900px;
  }
}

</style>
