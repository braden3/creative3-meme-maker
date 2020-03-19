<template>
  <div>
    <div class="wrapper">
      <div class="search">
        <form class="pure-form">
          <i class="fas fa-search"></i><input v-model="searchText" />
        </form>
      </div>
    </div>
    <MemeList :memes="memes" />
  </div>
</template>

<script>
// @ is an alias to /src
import MemeList from "../components/MemeList.vue"
export default {
  name: 'Home',
  components: {
    MemeList
  },
  data() {
    return {
      searchText: '',
    }
  },
  computed: {
    memes() {
      return this.$root.$data.memes.filter(meme => meme.name.toLowerCase().search(this.searchText) >= 0);
    }
  },
}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  color: orange;
  text-align: center;
}

.search {
  border: 1px solid #ccc;
  border-radius: 4px;
  width: 50%;
}

form {
  display: table;
  width: 100%;
}

i {
  display: table-cell;
  padding-left: 10px;
  width: 1px;
}

input {
  display: table-cell;
  font-size: 20px;
  border: none !important;
  box-shadow: none !important;
  width: 100%;
  height: 40px;
}
</style>
