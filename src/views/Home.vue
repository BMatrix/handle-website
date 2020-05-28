<template>
  <div class="home">
    <Header
      :backgroundimage="'images/enviroments/enviroment1.jpg'"
      :activepage="0"
      :buttonlink="'About'"
    >
      <template v-slot:title>{{ text.title }}</template>
      <template v-slot:subtitle>{{ text.subtitle }}</template>
      <template v-slot:button>{{ text.buttontext }}</template>
    </Header>
    <div class="productidea">
      <h2>{{ text.header1 }}</h2>
      <p>{{ text.paragraph1 }}</p>
      <Galery
        class="galery"
        :image11="'images/models/model1.png'"
        :image12="'images/models/model2.png'"
        :image13="'images/models/model3.png'"
        :image21="'images/enviroments/enviroment1.jpg'"
        :image22="'images/enviroments/enviroment2.jpg'"
        :image23="'images/enviroments/enviroment1.jpg'"
        :image31="'images/posters/poster1.jpg'"
        :image32="'images/posters/poster2.png'"
        :image33="'images/posters/poster3.png'"
      ></Galery>
    </div>
    <div class="team">
      <h2>{{ text.header2 }}</h2>
      <div id="members">
        <member
          class="member"
          :redscale="true"
          :background="true"
          :image="'images/team/AleksandraLobka.jpg'"
        >
          <template v-slot:name>Aleksandra Lobka</template>
          <template v-slot:role>{{ text.aleksandra_title }}</template>
          <template v-slot:description>{{ text.aleksandra_description }}</template>
        </member>
        <member class="member" :reverse="true" :image="'images/team/BenVinck.jpg'">
          <template v-slot:name>Ben Vinck</template>
          <template v-slot:role>{{ text.ben_title }}</template>
          <template v-slot:description>{{ text.ben_description }}</template>
        </member>
        <member class="member" :background="true" :image="'images/team/DarioVanMechelen.png'">
          <template v-slot:name>Dario Van Mechelen</template>
          <template v-slot:role>{{ text.dario_title }}</template>
          <template v-slot:description>{{ text.dario_description }}</template>
        </member>
        <member
          class="member"
          :reverse="true"
          :redscale="true"
          :image="'images/team/EricGonzales.jpg'"
        >
          <template v-slot:name>Eric Gonzales</template>
          <template v-slot:role>{{ text.eric_title }}</template>
          <template v-slot:description>{{ text.eric_description }}</template>
        </member>
        <member
          class="member"
          :redscale="true"
          :background="true"
          :image="'images/team/JoyAgwunedu.jpg'"
        >
          <template v-slot:name>Joy Agwunedu</template>
          <template v-slot:role>{{ text.joy_title }}</template>
          <template v-slot:description>{{ text.joy_description }}</template>
        </member>
        <member class="member" :reverse="true" :image="'images/team/MadelinaGavril.jpg'">
          <template v-slot:name>Madalina Gavril</template>
          <template v-slot:role>{{ text.madalina_title }}</template>
          <template v-slot:description>{{ text.madalina_description }}</template>
        </member>
        <member
          class="member"
          :redscale="true"
          :background="true"
          :image="'images/team/MarioGomezCarnero.jpg'"
        >
          <template v-slot:name>Mario Gomez Carnero</template>
          <template v-slot:role>{{ text.mario_title }}</template>
          <template v-slot:description>{{ text.mario_description }}</template>
        </member>
        <member class="member" :reverse="true" :image="'images/team/Sara-GülKangöz.jpg'">
          <template v-slot:name>Sara-Gül Kangöz</template>
          <template v-slot:role>{{ text.sara_gul_title }}</template>
          <template v-slot:description>{{ text.sara_gul_description }}</template>
        </member>
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
.productidea .galery {
  margin: 2em 0 2em 0;
}

.team h2 {
  margin-left: auto;
  margin-right: auto;
  width: 80%;
}

.home .interested {
  left: 50%;
  margin: 2em 0 2em 0;
}
</style>

<script>
import { Home } from "../lang/en.js";
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
  },
  data() {
    return {
      text: new Home()
    };
  }
};
</script>