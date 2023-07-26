<template>
  <div>
    <div class="rick-and-morti-header">
      <nuxt-link to="/" class="logo">
        <Logo />
      </nuxt-link>
      <div class="rick-and-morti-header__right">
        <nuxt-link class="rick-and-morti-header__link" to="/characters">
          Characters
        </nuxt-link>
        <nuxt-link to="/locations">Locations</nuxt-link>
        <nuxt-link to="/episodes">Episodes</nuxt-link>
      </div>
    </div>
    <nuxt />
  </div>
</template>

<script>
import Logo from "~/static/logoRickAndMorti.svg?inline";
export default {
  components: { Logo },
};
</script>

<style lang="css" scoped>
body {
  margin: 0 auto;
}
.rick-and-morti-header {
  display: flex;
  padding: 10px;
  justify-content: space-between;
  background-color: white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
.logo {
  margin-left: 150px;
}
.rick-and-morti-header a {
  float: left;
  color: black;
  text-align: center;
  text-decoration: none;
  font-size: 18px;
  line-height: 25px;
  border-radius: 4px;
  font-size: 23px;
}

.rick-and-morti-header__right {
  display: flex;
  gap: 30px;
  align-items: center;
  margin-right: 150px;
  color: black;
  font-weight: 600;
}

@media screen and (max-width: 500px) {
  .rick-and-morti-header a {
    display: block;
    text-align: left;
  }
}
</style>
