<template>
<div>
  <div class="welcome">
    Welcome  To Your Favorite Memes Page!!
  </div>
  <br>
  <hr>
  <br>
  <div id='nofavorites' v-show="this.$root.$data.favorites.length===0">You Currently Have No Favorites, Go Back To Home Page To Add Favorites</div>
  <div class="wrapper">
    <div class="favorites">
      <div class="meme" v-for="meme in Favorites" :key="meme.id">
        <div class="image">
          <img :src="'/images/'+meme.image">
        </div>
        <div class="info">
          <h1>{{meme.caption}}</h1>
        </div>
        <div class="favorite">
          <button class="auto" v-on:click="removefromfavorites(meme) ">Remove From Favorites</button>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Favorites',
  props: {
    favorites: Array
  },
  computed: {
    Favorites () {
      return this.$root.$data.favorites
    }
  },
  methods: {
    removefromfavorites(meme) {
      for(let i = 0; i < this.$root.$data.favorites.length; i++){
        if(this.$root.$data.favorites[i] === meme){
          this.$root.$data.favorites.splice(i,1);
          break;
        }
      }
    }
  }
}

</script>

<style>
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
  width: 50%;
  margin: auto;
}

.meme img {
  border: 2px solid #333;
  width: 100%;
  object-fit: cover;
  height: 100%;
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

.favorite {
  color: white;
}

</style>
