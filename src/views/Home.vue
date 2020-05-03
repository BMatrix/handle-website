<template>
  <div class="home">
    <div class="center">
      <div class="head">
        <h1>You can Handle It!</h1>
      </div>
    </div>
    <div class="main">
      <div class="center">
        <div class="content">
          <img src="models/model1.png">
          <div>
            <h2>Title Here</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem necessitatibus voluptas fugit quaerat nemo quos, aut at eum voluptatum, reiciendis, eos illum dolor corrupti quasi odio architecto adipisci maxime fugiat.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
.home {
  background-color: #f61f28;
  height: 100%;
}

.center {
  margin-left: auto;
  margin-right: auto;
  width: 70%;
  text-align: center;
}

.head {
  margin-top: 2em;
  margin-bottom: 2em;
  width: 80%;
  height: 500px;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  flex-direction: column;
  justify-content: end;
  background-image: url("../../public/enviroments/enviroment1.jpg");
  background-position: center bottom;
  background-size: cover;
  border: solid black 5px;
  color: white;
  font-size: 1.25em;
}
.head h1 {
  align-self: start;
  padding: 0 0 1.2em 1.5em;
}

.main {
  position: absolute;
  width: 100%;
  height: auto;
  background-color: white;
}

.content{
  padding: 2em 0 2em 0;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.content img{
  width: 40%;
  flex-shrink: 0;
}
.content div{
  display:flex;
  flex-direction: column;
  justify-content: center;
  text-align: left;
  padding-left: 10%;
}
</style>