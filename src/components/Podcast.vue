<template>
  <div class="site-wrap" v-if="podcast"></div>
</template>  


<script>
import PodcastsFooter from "./PodcastsFooter";
import PodcastsHeader from "./PodcastsHeader";
import {mapState, mapActions } from "vuex";

export default {
  name: "Podcast",
  components: { PodcastsFooter, PodcastsHeader },
  
created() {
    this.loadPodcast(this.$route.params.id);
},
computed:{...mapState(['podcast'])},
methods: {
        ...mapActions(['loadPodcast'])
},
};
</script>
