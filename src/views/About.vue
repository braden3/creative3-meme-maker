<template>
  <div>
    <div class="welcome">
      Click one of the images to download!!
    </div>
    <br>
    <hr>
    <br>
    <div class="row">
      <div class="column" style="background-color:#aaa;">
        <h2>Philosoraptor</h2>
        <a href="/images/walk-on-water.jpg" download>
          <img src="/images/walk-on-water.jpg">
        </a>
        <!--h2>Column 1</h2-->
        <!--button id='starwars' v-on:click="showstarwarsmemes()">Star Wars</button-->
      </div>
      <div class="column" style="background-color:#bbb;">
        <!--h2>Column 2</h2-->
        <h2>Dew It</h2>
        <a href="/images/dew-it.jpg" download>
          <img src="/images/dew-it.jpg">
        </a>
        <!--button>Philosoraptor</button-->
      </div>
      <div class="column" style="background-color:#aaa;">
        <h2>Unsettled Tom</h2>
        <!--h2>Column 3</h2-->
        <!--button>Unsettled Tom</button-->
        <a href="/images/petco.jpg" download>
          <img src="/images/petco.jpg">
        </a>
      </div>
    </div>
  </div>
</template>

<!--<a href="/images/baby-yoda.jpg" download>
  <img src="/images/baby-yoda.jpg">
</a>-->

<script>
//methods: {
  //showstarwarsmemes () {
    //let starwarsmemes = '<img src="/images/baby-yoda.jpg"/>';
    //getElementById('starwars').innerHTML = starwarsmemes;
  //}
//}



</script>

<style>

* {
  box-sizing: border-box;
}

.row {
  display: flex;
}

.welcome {
  background-color: #42b983;
  height: 50px;
  width: 50%;
  margin: auto;
  border: solid 3px;
  text-align: center;
  line-height: 50px;
  font-weight: bold;
}

hr {
  width: 75%;
  margin: auto;
}

/* Create two equal columns that sits next to each other */
.column {
  flex: 33%;
  padding: 10px;
  height: 400px; /* Should be removed. Only for demonstration */
  color: white;
}

img {
  padding-top: 30px;
  width: 75%;
  height: 250px;
}

button {
  color: white;
}



</style>
