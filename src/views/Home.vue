<template>
  <v-container
    grid-list-lg
  >
    <v-layout
      row
      wrap
    >
      <v-flex
        xs12
      >
        <Intro data-aos="fade" />
      </v-flex>
      <!--      <v-flex-->
      <!--        xs12-->
      <!--        sm6-->
      <!--      >-->
      <!--        <Contact-->
      <!--          data-aos="fade"-->
      <!--        />-->
      <!--      </v-flex>-->
      <v-flex
        xs12
        md6
      >
        <Contribute
          data-aos="fade"
        />
      </v-flex>
      <v-flex
        xs12
        md6
      >
        <Donate
          data-aos="fade"
        />
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import Contribute from "@/views/About/Contribute";
import Donate from "@/views/About/Donate";
import Intro from "@/views/About/Intro";
export default {
  name: "Home",
  components: { Contribute, Donate, Intro },
  data: () => ({}),
  methods: {
    goToPage(name) {
      this.$router.push({ name: name })
    }
  }
};
</script>

<style scoped>
.home-card {
  height: 100%;
}
</style>