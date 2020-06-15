<template>
  <div class="team">
    <Header :backgroundimage="'images/headers/Team.jpg'" :activepage="2">
      <template v-slot:title>
        <h1>{{ text.title }}</h1>
      </template>
      <template v-slot:subtitle>{{ text.subtitle }}</template>
      <template v-slot:button>{{ text.buttontext }}</template>
    </Header>
    <div class="teamsection">
      <TitleOverlined>
        <h2>{{ text.team_header }}</h2>
      </TitleOverlined>
      <div class="members">
        <member class="member" :redscale="true" :image="'images/team/AleksandraLobka.jpg'">
          <template v-slot:name>Aleksandra Lobka</template>
          <template v-slot:role>{{ text.aleksandra_title }}</template>
          <template v-slot:quote>{{ text.aleksandra_quote }}</template>
        </member>
        <member class="member" :image="'images/team/BenVinck.jpg'">
          <template v-slot:name>Ben Vinck</template>
          <template v-slot:role>{{ text.ben_title }}</template>
          <template v-slot:quote>{{ text.ben_quote }}</template>
        </member>
        <member class="member" :image="'images/team/DarioVanMechelen.png'">
          <template v-slot:name>Dario Van Mechelen</template>
          <template v-slot:role>{{ text.dario_title }}</template>
          <template v-slot:quote>{{ text.dario_quote }}</template>
        </member>
        <member class="member" :redscale="true" :image="'images/team/EricGonzales.jpg'">
          <template v-slot:name>Eric Gonzales</template>
          <template v-slot:role>{{ text.eric_title }}</template>
          <template v-slot:quote>{{ text.eric_quote }}</template>
        </member>
        <member class="member" :redscale="true" :image="'images/team/JoyAgwunedu.jpg'">
          <template v-slot:name>Joy Agwunedu</template>
          <template v-slot:role>{{ text.joy_title }}</template>
          <template v-slot:quote>{{ text.joy_quote }}</template>
        </member>
        <member class="member" :image="'images/team/MadelinaGavril.jpg'">
          <template v-slot:name>Madalina Gavril</template>
          <template v-slot:role>{{ text.madalina_title }}</template>
          <template v-slot:quote>{{ text.madalina_quote }}</template>
        </member>
        <member class="member" :redscale="true" :image="'images/team/MarioGomezCarnero.jpg'">
          <template v-slot:name>Mario Gomez Carnero</template>
          <template v-slot:role>{{ text.mario_title }}</template>
          <template v-slot:quote>{{ text.mario_quote }}</template>
        </member>
        <member class="member" :image="'images/team/Sara-GülKangöz.jpg'">
          <template v-slot:name>Sara-Gül Kangöz</template>
          <template v-slot:role>{{ text.sara_gul_title }}</template>
          <template v-slot:quote>{{ text.sara_gul_quote }}</template>
        </member>
      </div>
    </div>
    <Interested class="interested"></Interested>
  </div>
</template>

<style scoped>
h2 {
  font-size: 2em;
  padding: 0.5em 0 0.5em 0.3em;
}

.teamsection {
  margin: 2em auto 4em auto;
  width: 80%;
}

.members {
  display: flex;
  flex-grow: 1;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
}
.members .member {
  width: 45%;
  margin-bottom: 2em;
}
</style>

<script>
import { Team } from "../lang/en.js";
import Header from "../components/Header.vue";
import TitleOverlined from "../components/TitleOverlined.vue";
import Member from "../components/Member.vue";
import Interested from "../components/Interested.vue";
export default {
  components: {
    Header,
    TitleOverlined,
    Member,
    Interested
  },
  data() {
    return {
      text: new Team()
    };
  }
};
</script>