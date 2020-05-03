<template>
  <div class="team">
    <div class="center">
      <h1>The Team</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur laborum adipisci, voluptatum laboriosam nesciunt ex commodi voluptatem similique accusamus totam cupiditate sint, voluptas harum, iusto tempora libero reiciendis distinctio alias!</p>
      <div id="members">
        <member class="member"                   :redscale="true"  :image="'team/AleksandraLobka.jpg'">    <template v-slot:name>Aleksandra Lobka</template>     <template v-slot:role>Architecture Engineering</template>   <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"  :reverse="true"                    :image="'team/BenVinck.jpg'">           <template v-slot:name>Ben Vinck</template>            <template v-slot:role>Electronics and ICT</template>        <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"                                     :image="'team/DarioVanMechelen.png'">   <template v-slot:name>Dario Van Mechelen</template>   <template v-slot:role>Graphic and Digital Media</template>  <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"  :reverse="true"  :redscale="true"  :image="'team/EricGonzales.jpg'">       <template v-slot:name>Eric Gonzales</template>        <template v-slot:role>Industrial Design</template>          <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"                   :redscale="true"  :image="'team/JoyAgwunedu.jpg'">        <template v-slot:name>Joy Agwunedu</template>         <template v-slot:role>Multimedia Production</template>      <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"  :reverse="true"                    :image="'team/MadelinaGavril.jpg'">     <template v-slot:name>Madelina Gavril</template>      <template v-slot:role>Advertising</template>                <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"                   :redscale="true"  :image="'team/MarioGomezCarnero.jpg'">  <template v-slot:name>Mario Gomez Carnero</template>  <template v-slot:role>Industrial Design</template>          <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
        <member class="member"  :reverse="true"                    :image="'team/Sara-GülKangöz.jpg'">     <template v-slot:name>Sara-Gül Kangöz</template>      <template v-slot:role>Media and Communications</template>   <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, eos voluptates explicabo dolor delectus enim debitis similique maxime assumenda pariatur ad vero optio earum, tempore numquam placeat atque distinctio accusamus.</template></member>
      </div>
    </div>
  </div>
</template>

<style scoped>
.center {
  margin-top: 1em;
  margin-left: auto;
  margin-right: auto;
  width: 70%;
  text-align: center;
}
#members{
  margin-top: 3em;
}
</style>

<script>
import Member from "../components/Member.vue";
export default {
  components: {
    Member
  }
};
</script>