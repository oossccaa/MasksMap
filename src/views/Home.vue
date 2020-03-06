<template>
  <div style="height:100%" class="home">
    <Map style="height:100%" />
  </div>
</template>

<script>
// @ is an alias to /src
import Map from "@/components/Map";

export default {
  name: "Home",
  components: {
    Map
  }
};
</script>
