<template>
  <div class="about">
    <div class="center">
      <img src="models/model3.png" />
    </div>
    <div class="wide">
      <div class="center">
        <h2>Title Here</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Esse expedita fuga, explicabo mollitia commodi dignissimos eligendi! Quia eveniet natus in culpa vero vel deserunt error minus fuga. Laboriosam, eveniet tempore! Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quisquam nobis accusamus facilis voluptatum, veniam voluptatibus. Ratione numquam velit perspiciatis a? Aperiam magnam praesentium odio minus earum iste vero sed delectus. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis dolores nemo, earum autem voluptatum beatae mollitia doloremque non perspiciatis ipsam odit laudantium, veritatis aperiam corrupti, aliquid inventore laboriosam eveniet aspernatur? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium nesciunt, ea laborum ipsum atque officiis minima vitae fuga facere cupiditate error doloribus tenetur dignissimos ut odio porro voluptatem vero placeat.</p>
      </div>
      <div class="center">
        <div class="extra">
          <img src="enviroments/enviroment2.jpg" />
          <div>
            <h2>Title Here</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum dicta facere asperiores ipsa explicabo, harum dolorem provident cumque. Iste in quos ullam est illo eius beatae reiciendis autem modi suscipit. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus id asperiores molestiae ab voluptates laboriosam, nesciunt quos nisi, eius dicta quis fuga, ipsa eaque? Aperiam distinctio quibusdam accusantium illo quas. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Fugit, dolorum voluptas?</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about {
  height: 100%;
}

.center {
  margin-left: auto;
  margin-right: auto;
  width: 70%;
  text-align: center;
}

.center > img {
  padding: 2em 0 2em 0;
  width: 80%;
}

.wide {
  background-color: #f61f28;
  width: 100%;
  height: auto;
  padding: 2em 0 2em 0;
}

.extra {
  margin-top: 2em;
  display: flex;
  flex-direction: row-reverse;
  background-color: white;
  padding: 1em;
}
.extra img {
  flex-shrink: 0;
  width: 40%;
}
.extra div {
  align-self: center;
  text-align: right;
  padding: 0 10% 0 0;
  display: flex;
  flex-direction: column;
}
</style>