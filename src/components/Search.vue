<template>
  <div class="searchContainer">
    <div>
      <div class="logoS"> 
        Home Page
      </div>
      <div class="Ssec">
        <div class="inputContainer">
          <img width="50" height="50" src="/duckduckgo.svg" />
          <input v-model="searchValue" type="text" placeholder="Search"/>
        </div>
        <div @click="enter" class="enterButton">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="m19.6 21l-6.3-6.3q-.75.6-1.725.95T9.5 16q-2.725 0-4.612-1.888T3 9.5q0-2.725 1.888-4.612T9.5 3q2.725 0 4.612 1.888T16 9.5q0 1.1-.35 2.075T14.7 13.3l6.3 6.3l-1.4 1.4ZM9.5 14q1.875 0 3.188-1.313T14 9.5q0-1.875-1.313-3.188T9.5 5Q7.625 5 6.312 6.313T5 9.5q0 1.875 1.313 3.188T9.5 14Z"/></svg>
        </div>
      </div>
    </div>
    <FavWebsites />
  </div>
</template>

<script>
import { ref } from "vue"
import FavWebsites from "./FavWebsites.vue"

export default {
  components: {
    FavWebsites
  },
  data() {
    return {
      searchValue: ref(""),
    }
  },
  methods: {
    enter() {
      console.log(this.searchValue);
      window.location.href = "https://www.duckduckgo.com/?q=" + this.searchValue;
    }
  }
}

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@600&display=swap');

.searchContainer {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  z-index: 999;
  flex-direction: column;
}
.inputContainer > input {
  background: #333333;
  width: 300px;
  height: 50px;
  z-index: 10;
  border: none;
  font-size: 15px;
  color: #aaaaaa;
  font-family: "Noto Sans", sans-serif;
}
.Ssec {
  z-index: 10;
  width: 500px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 20px;
}
.searchContainer > div {
  z-index: 10;
  background: #282828;
  border-radius: 20px;
  height: 200px;
}
.inputContainer > input:focus {
  outline: none;
}
.inputContainer {
  display: flex;
  border-radius: 10px 5px 5px 10px;
  background: #333333;
}
.inputContainer > * {
  margin: 4px;
}
.enterButton {
  margin-left: 2px;
  background: #333333;
  height: 52px;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50px;
  border-radius: 5px 10px 10px 5px;
  padding: 4px;
  color: #fff;
  cursor: pointer;
}
.enterButton:hover {
  background: #3a3a3a;
}
.logoS {
  font-size: 30px;
  color: #fff;
  font-family: 'Titillium Web', sans-serif;
  background: #333333;
  width: 428px;
  margin-bottom: 2px;
  border-radius: 10px;
  text-align: center;
  margin-top: 30px;
  margin-left: auto;
  margin-right: auto;
  height: 80px;
  background: linear-gradient(
    to bottom,
    #282828,
    #333333
  );
}
</style>

