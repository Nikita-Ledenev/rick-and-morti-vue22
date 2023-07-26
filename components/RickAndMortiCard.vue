<template>
  <div class="rick-and-morti-card">
    <div
      class="rick-and-morti-card__container"
      v-for="character in characters"
      :key="character.id"
    >
      <img
        class="rick-and-morti-card__img"
        :src="character.image"
        alt="1123123"
      />
      <div class="rick-and-morti-card__title">
        {{ character.name }}
      </div>
      <div class="rick-and-morti-card__gender">
        {{ character.gender }}
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      characters: [],
    };
  },
  mounted() {
    this.getCharasters();
  },
  methods: {
    async getCharasters() {
      const apiUrl = "https://rickandmortyapi.com/api/character?page=3";
      axios
        .get(apiUrl)
        .then((response) => {
          this.characters = response.data.results;
        })
        .catch((error) => {
          console.error("Error fetching characters:", error);
        });
    },
  },
};
</script>

<style lang="css" scoped>
.rick-and-morti-card {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(2, 1fr);
  grid-column-gap: 25px;
  grid-row-gap: 30px;
  margin-top: 20px;
}
.rick-and-morti-card__container {
  border: 1px solid black;
  border-radius: 15px;
  width: 240px;
  height: 244px;
}
.rick-and-morti-card__title {
  margin-left: 20px;
  margin-top: 10px;
  color: black;
}
.rick-and-morti-card__img {
  width: 240px;
  height: 160px;
  border-radius: 15px;
}
.rick-and-morti-card__gender {
  margin-left: 20px;
  margin-top: 10px;
  color: black;
}
</style>
