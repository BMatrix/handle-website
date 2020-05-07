<template>
  <div class="about">
    <Header :backgroundimage="'models/model3.png'" :activepage="1">
      <template v-slot:title>About</template>
      <template
        v-slot:text
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora quisquam assumenda obcaecati veniam reprehenderit ad, ullam, necessitatibus nostrum nemo error et placeat aliquam non magnam delectus corrupti enim doloribus molestiae?</template>
    </Header>
    <div class="information">
      <DescribedImage class="work" :image="'enviroments/enviroment1.jpg'" :reverse="true">
        <template v-slot:title>Title Here</template>
        <template
          v-slot:text
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe earum aperiam aliquid laboriosam dolores voluptatem, ea, quo expedita numquam enim fuga veritatis adipisci placeat perferendis? Ea excepturi a qui et. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Autem beatae nam quibusdam aperiam sed laborum ducimus eaque quasi ad incidunt! Consectetur sapiente atque placeat dicta velit officia eos vel et? Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsam, odio possimus. Eaque officia iusto fuga placeat recusandae deleniti, quis delectus doloremque distinctio quae sequi ipsum odit expedita fugiat praesentium illum. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Unde doloribus delectus, asperiores, beatae repellendus at amet fugiat commodi accusantium cum necessitatibus ad quam possimus exercitationem officia, ut odit optio nesciunt.</template>
      </DescribedImage>
      <DescribedImage class="work" :image="'enviroments/enviroment2.jpg'">
        <template v-slot:title>Title Here</template>
        <template
          v-slot:text
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe earum aperiam aliquid laboriosam dolores voluptatem, ea, quo expedita numquam enim fuga veritatis adipisci placeat perferendis? Ea excepturi a qui et. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Autem beatae nam quibusdam aperiam sed laborum ducimus eaque quasi ad incidunt! Consectetur sapiente atque placeat dicta velit officia eos vel et? Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsam, odio possimus. Eaque officia iusto fuga placeat recusandae deleniti, quis delectus doloremque distinctio quae sequi ipsum odit expedita fugiat praesentium illum. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Unde doloribus delectus, asperiores, beatae repellendus at amet fugiat commodi accusantium cum necessitatibus ad quam possimus exercitationem officia, ut odit optio nesciunt.</template>
      </DescribedImage>
    </div>
    <Interested class="interested"></Interested>
  </div>
</template>

<style scoped>
.about {
  height: 100%;
}

.information * {
  margin: 4em 0 4em 0;
}

.interested {
  margin: 8em 0 8em 0;
}
</style>

<script>
import Header from "../components/Header.vue";
import DescribedImage from "../components/DescribedImage.vue";
import Interested from "../components/Interested.vue";
export default {
  components: {
    Header,
    DescribedImage,
    Interested
  }
};
</script>