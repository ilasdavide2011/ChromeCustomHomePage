<template>
  <div class="main">
    <div class="container">
      <a href="https://www.youtube.com/">
        <p>Youtube</p>
        <span>https://www.youtube.com/</span>
      </a>
      <a href="https://github.com/">
        <p>Github</p>
        <span>https://github.com/</span>
      </a>
      <a href="https://www.wikipedia.org/">
        <p>Wikipedia</p>
        <span>https://www.wikipedia.org/</span>
      </a>
      <a href="https://twitter.com/home">
        <p>Twitter</p>
        <span>https://twitter.com/home</span>
      </a>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@600&display=swap');

.main {
  background: #232323;
  border-radius: 20px;
  margin-top: 15px;
  width: 500px;
}
.main > .container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  margin: 20px;
  width: 460px;
  height: 160px;
}
.main > .container > a {
  margin: 2px;
  background: #333333;
  border-radius: 5px;
  font-family: 'Titillium Web', sans-serif;
  text-decoration: none;
  color: #fff;
}
.main > .container > a:hover {
  background: #3a3a3a
}
.main > .container > a > p {
  font-size: 20px;
  margin-left: 10px;
  margin-top: 10px;
}
.main > .container > a > span {
  margin-left: 10px;
  color: #aaaaaa;
}
* {
  text-decoration: none;
  color: inherit;
}
</style>
