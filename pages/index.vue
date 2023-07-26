<template>
  <div class="rick-and-morti">
    <RickAndMortiMainVue />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import RickAndMortiMainVue from "~/components/RickAndMortiMain.vue";

export default Vue.extend({
  layout: "RickAndMortiHeader",
  components: { RickAndMortiMainVue },
  name: "rick-and-morti",
});
</script>
<style scroped></style>
