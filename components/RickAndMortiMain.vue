<template>
  <div class="rick-and-morti-main">
    <div class="rick-and-morti-main__container">
      <img class="rick-and-morti-main__logo" src="~/static/logoMain.svg" />
      <RickAndMortiCard />
    </div>
  </div>
</template>

<script>
import RickAndMortiCard from "~/components/RickAndMortiCard";
export default {
  components: { RickAndMortiCard },
};
</script>

<style lang="css">
.rick-and-morti-main {
  display: flex;
  margin: 35px 150px 0px 150px;
  justify-content: center;
  align-items: center;
  font-size: 20px;
  font-weight: 600;
  color: green;
}
.rick-and-morti-main__logo {
  margin: 35px 150px 0px 245px;
  display: flex;
  align-items: center;
}
</style>
