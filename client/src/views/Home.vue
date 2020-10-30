<template>
  <div>
    <h1>This is the Home page</h1>
    <GuitarFretboard />
  </div>
</template>

<script>
import GuitarFretboard from "../components/GuitarFretboard.vue";

export default {
  name: "Home",
  components: {
    GuitarFretboard,
  },
};
</script>