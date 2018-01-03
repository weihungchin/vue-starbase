<template>
  <div id = "app" class = "container">
   <h3>{{title}}</h3>

   <div class = "row">

   <Character 
   v-for="(id, index) in initial_ids" 
   v-bind:id = "id" 
   :key="index"
   />
   </div>

  <h4>
    <router-link to = "/data/people">Meet the Characters</router-link>&nbsp;|&nbsp;
    <router-link to = "/data/planets">Explore the Planets</router-link>
  </h4>
  <router-view></router-view>

</div>
</template>


<script>
import Character from "./components/Character.vue";
import Data from "./components/Data.vue";

export default {
  name: "app",
  data() {
    return {
      title: "Generate Your Team",
      initial_ids: [1, 13, 14]
    };
  },
  components: {
    Character,
    Data
  }
};
</script>



