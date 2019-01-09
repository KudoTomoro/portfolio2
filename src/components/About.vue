<template>
<div class="wrapper">
  <h1>
    About
  </h1>
  <div class="container mt-5 px-1">
    <div class="mt-5 mb-5">
      <h2>工藤 友郎<span>KUDO TOMORO</span></h2>
      <div class="introduction mt-4">
        <p>1997年生まれ。実家は宮城県です。大学から上京し、2018年秋から2019年夏まで中国の杭州に留学中です。ブロックチェーンと服が好きです。好きなスマホアプリはTwitterとWEAR。</p>
      </div>
    </div>

    <div>
      <div class="my-5 py-5">
        <h2>SNS</h2>
        <div class="about-sns">
          <a class="m-3" href="https://twitter.com/tomoro_2">
            <i class="fab fa-twitter fa-3x"></i>
          </a>
          <a class="m-3" href="https://github.com/KudoTomoro">
            <i class="fab fa-github fa-3x"></i>
          </a>
          <a class="m-3" href="https://www.instagram.com/tomoro5656/">
            <i class="fab fa-instagram fa-3x"></i>
          </a>
        </div>
      </div>
    </div>

    <div class="skill mt-5">
      <h2>Skills<span>開発言語/フレームワーク/その他</span></h2>

      <div class="skillbutton my-4">
            <b-btn class="m-2" variant="outline-secondary">HTML/CSS</b-btn>
            <b-btn class="m-2" variant="outline-secondary">Bootstrap</b-btn>
            <b-btn class="m-2" variant="outline-secondary">Javascript</b-btn>
            <b-btn class="m-2" variant="outline-secondary">Vue.js</b-btn>
            <b-btn class="m-2" variant="outline-secondary">jQuery</b-btn>
            <b-btn class="m-2" variant="outline-secondary">Wordpress</b-btn>
            <b-btn class="m-2" variant="outline-secondary">中国語</b-btn>
            <b-btn class="m-2" variant="outline-secondary">英語</b-btn>
      </div>
    </div>

  <!-- <div id="wp">
    <posts></posts>
  </div> -->


  </div>

</div>
</template>

<script>

</script>

<style lang="scss" scoped>
.container{
  width:800px;
  margin-left:auto;
  margin-right: auto;
  padding-left: 5%;
}

h1{
  width:800px;
  margin-left:auto;
  margin-right: auto;
 text-align: center;
}

.introduction{
  width:750px;
  // margin-left:auto;
  // margin-right: auto;
}

h2, p{
  text-align: left;
  line-height: 2rem;
}

span{
  font-size: 12px;
  color: #6b6d6d;
  margin-left: 15px;
}

.about-sns a{
  color:#ff4488;
}

.skill{
  padding-bottom: 50px;
}

.skillbutton button{
  width:120px;
}

.skillbutton{
width:700px;
}

@media (max-width:420px){
  .container{
    width:300px;
  }

  h1{
    width:300px;
    margin-left:auto;
    margin-right: auto;
   text-align: center;
  }

  .introduction{
    width:300px;
  }

  .skillbutton{
  width:300px;
  margin-right: 20px;
  }
}

@media screen and (min-width:450px) and ( max-width:770px){
  .container, .introduction, .skillbutton{
    width:500px;
  }
}
</style>
