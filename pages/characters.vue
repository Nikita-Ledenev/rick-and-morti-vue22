<template>
  <section>
    <div class="rick-and-morti-characters">
      <div class="rick-and-morti-characters__container">
        <img class="rick-and-morti-main__logo" src="~/static/logoMain.svg" />
        <RickAndMortiCard />
      </div>
    </div>
  </section>
</template>

<script>
import RickAndMortiCard from "~/components/RickAndMortiCard.vue";
export default {
  components: { RickAndMortiCard },
  layout: "RickAndMortiHeader",
};
</script>

<style lang="css" scoped>
.rick-and-morti-characters {
  display: flex;
  justify-content: center;
  align-items: center;
}
.rick-and-morti-main__logo {
  border-radius: 15px;
  margin-top: 80px;
}
</style>
