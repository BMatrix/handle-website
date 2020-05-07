<template>
  <div class="home">
    <Header :backgroundimage="'enviroments/enviroment1.jpg'" :activepage="0" :toolbarcolor="'#FF000060'">
      <template v-slot:title>You Can Hande it!</template>
    </Header>
    <div class="productidea">
      <h2>The Product Idea</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur sequi suscipit odit molestiae itaque cum! Dolore recusandae perspiciatis eaque, sequi, harum aspernatur doloribus ullam quae beatae numquam cum impedit deserunt! Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum iusto dolorum eaque placeat commodi a sapiente consectetur corporis voluptatem nam. Exercitationem ea officia commodi excepturi quaerat tempore tempora odio architecto. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deleniti nam deserunt expedita quo dolor natus quidem placeat reprehenderit voluptatum atque eum, animi voluptatibus at ex iure odio illo voluptatem totam? Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto, dolorem autem expedita vel amet sint modi eum repellat accusamus in aliquid iure recusandae sed ea aperiam, nam eligendi! Blanditiis, ex? Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur laudantium quod deleniti debitis ducimus reiciendis obcaecati mollitia a, incidunt molestiae ullam voluptate itaque, sit officia eveniet iusto quae neque vel.</p>
      <Galery
        class="galery"
        :image11="'models/model1.png'"
        :image12="'models/model2.png'"
        :image13="'models/model3.png'"
        :image21="'enviroments/enviroment1.jpg'"
        :image22="'enviroments/enviroment2.jpg'"
        :image23="'enviroments/enviroment1.jpg'"
        :image31="'posters/poster1.jpg'"
        :image32="'posters/poster2.png'"
        :image33="'posters/poster3.png'"
      ></Galery>
    </div>
    <div class="team">
      <h2>Meet our Team!</h2>
      <div id="members">
        <member class="member"                   :redscale="true"  :background="true"  :image="'team/AleksandraLobka.jpg'">    <template v-slot:name>Aleksandra Lobka</template>     <template v-slot:role>Architecture Engineering</template>   <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"  :reverse="true"                                        :image="'team/BenVinck.jpg'">           <template v-slot:name>Ben Vinck</template>            <template v-slot:role>Electronics and ICT</template>        <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"                                     :background="true"  :image="'team/DarioVanMechelen.png'">   <template v-slot:name>Dario Van Mechelen</template>   <template v-slot:role>Graphic and Digital Media</template>  <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"  :reverse="true"  :redscale="true"                      :image="'team/EricGonzales.jpg'">       <template v-slot:name>Eric Gonzales</template>        <template v-slot:role>Industrial Design</template>          <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"                   :redscale="true"  :background="true"  :image="'team/JoyAgwunedu.jpg'">        <template v-slot:name>Joy Agwunedu</template>         <template v-slot:role>Multimedia Production</template>      <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"  :reverse="true"                                        :image="'team/MadelinaGavril.jpg'">     <template v-slot:name>Madelina Gavril</template>      <template v-slot:role>Advertising</template>                <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"                   :redscale="true"  :background="true"  :image="'team/MarioGomezCarnero.jpg'">  <template v-slot:name>Mario Gomez Carnero</template>  <template v-slot:role>Industrial Design</template>          <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"  :reverse="true"                                        :image="'team/Sara-GülKangöz.jpg'">     <template v-slot:name>Sara-Gül Kangöz</template>      <template v-slot:role>Media and Communications</template>   <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
      </div>
    </div>
    <Interested class="interested"></Interested>
  </div>
</template>

<style scoped>
h2 {
  color: blue;
  font-size: 3em;
  padding: 0.5em 0 0.5em 0.3em;
}

.productidea {
  margin: 0 auto 0 auto;
  width: 80%;
}
.galery {
  margin: 2em 0 2em 0;
}

.team h2 {
  margin-left: auto;
  margin-right: auto;
  width: 80%;
}

.interested {
  left: 50%;
  margin: 2em 0 2em 0;
}
</style>

<script>
import Header from "../components/Header.vue";
import Galery from "../components/Galery.vue";
import Member from "../components/Member.vue";
import Interested from "../components/Interested.vue";
export default {
  components: {
    Header,
    Galery,
    Member,
    Interested
  }
};
</script>