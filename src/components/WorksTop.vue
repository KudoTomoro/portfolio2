<template>
  <div >
    <h1 class="workstop">Works</h1>
    <div class="container">
      <div class="row">
          <b-card v-for="d in data"  class="workcard border-info mb-3">
            <h3 class="card-text m-4">
              <router-link :to="'/works/' + d.slug">{{d.title}}</router-link>
            </h3>
            <p class="card-text pb-2" style="height: 14rem; text-align:left;">
              {{ d.text }}
            </p>
            <p class="cardbutton pb-2">
              <b-button class="px-5" href="#" variant="info">GitHub</b-button>
            </p>
          </b-card>

      </div>
    </div>

  </div>
</template>

<script>
// import box from '@/components/box.vue'

export default{
  title:'....',
  description:'....',
  props:['data']
}
</script>

<style lang="scss" scoped>
.workstop{
  margin-bottom: 0;
}

.row{
  margin-left: auto;
  margin-right: auto;
}

.row h3{
  font-weight: bold;
}

.workcard{
  width: 31rem;
  height: 26rem;
  margin:3rem;

}

.card-body{
  position: relative;
  display: inline-block;
}

.cardbutton{
  position: absolute;
  left:34%;
  bottom:0;
}


@media screen and (min-width:768px) and ( max-width:1024px) {
  .container{
    // background-color:#000644;
    margin-left: auto;
    margin-right: auto;
  }

  .row{
    margin-left: auto;
    margin-right: auto;
    // padding-left: 2rem;
  }


  .workcard{
    width: 26rem;
    height: 30rem;
    margin-left:20px;
  }

}

</style>
