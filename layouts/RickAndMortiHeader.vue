<template>
  <div>
    <div class="rick-and-morti-header">
      <a href="/" class="logo">CompanyLogo</a>
      <div class="rick-and-morti-header__right">
        <nuxt-link class="rick-and-morti-header__link" to="/characters"
          >Characters</nuxt-link
        >
        <nuxt-link to="/locations">Locations</nuxt-link>
        <nuxt-link to="/episodes">Episodes</nuxt-link>
      </div>
    </div>
    <nuxt />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.rick-and-morti-header {
  overflow: hidden;
  background-color: #f1f1f1;
  padding: 20px 10px;
}

.rick-and-morti-header a {
  float: left;
  color: black;
  text-align: center;
  padding: 12px;
  text-decoration: none;
  font-size: 18px;
  line-height: 25px;
  border-radius: 4px;
}

.rick-and-morti-header a.logo {
  font-size: 25px;
  font-weight: bold;
}

.rick-and-morti-header a:hover {
  background-color: green;
  color: black;
}

.rick-and-morti-header a.active {
  background-color: dodgerblue;
  color: white;
}

.rick-and-morti-header__right {
  float: right;
}

@media screen and (max-width: 500px) {
  .rick-and-morti-header a {
    float: none;
    display: block;
    text-align: left;
  }
  .rick-and-morti-header__right {
    float: none;
  }
}
</style>
