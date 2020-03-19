<template>
  <div>
    <div class="welcome">
      Click create meme to enter a caption, then switch to favorites tab to view meme!!
    </div>
    <br>
    <hr>
    <br>
    <div class="wrapper">
      <div class="memes">
        <div class="meme" v-for="meme in memes" :key="meme.id">
          <div class="info">
            <h1>{{meme.name}}</h1>
            <!--p>{{product.country}}</p-->
          </div>
          <div class="image">
            <img :src="'/images/'+meme.image">
          </div>
          <div class="favorite">
            <!--h2>{{product.price}}</h2-->
            <button class="auto" v-on:click="addtofavorites(meme)">Create Meme</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MemeList',
  props: {
    memes: Array
  },
methods: {
  addtofavorites(meme) {
    var tempcaption = prompt("Type in Meme Text:");
    meme.caption = tempcaption;
    this.$root.$data.favorites.push(meme)
    //this.$root.$data.numberOfItems +=1;
  }
}
}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.memes {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.meme {
  margin: 10px;
  margin-top: 50px;
  width: 200px;
}

.meme img {
  border: 2px solid #333;
  height: 250px;
  width: 200px;
  object-fit: cover;
}

.meme .image {
  display: flex;
  justify-content: center;
  margin-bottom: 5px;
}

.info {
  background: #96FFA4;
  color: #000;
  padding: 10px 30px;
  height: 80px;
}

.info h1 {
  font-size: 16px;
}

.info h2 {
  font-size: 14px;
}

.info p {
  margin: 0px;
  font-size: 10px;
}


.price {
  display: flex;
}

button {
  height: 50px;
  background: #000;
  color: white;
  border: none;
}

.auto {
  margin-left: auto;
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
  margin-top: 10px;
}
</style>
