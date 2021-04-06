<template>
  <div class="PitchDeck">
    <dialogs v-on:currentDialog="setCurrentDialog" />
    <doubt-slide v-if="currentDialog == 1" />
    <organization-slide v-if="currentDialog == 2" />
    <playlists-slide v-if="currentDialog == 3" />
    <lyrics-slide v-if="currentDialog == 4" />
    <mashups-slide v-if="currentDialog == 5" />
    <deezer-slide v-if="currentDialog == 6" />
    <other-features v-if="currentDialog == 7" />
    <final-slide v-if="currentDialog == 8" />
  </div>
</template>

<script>
import Dialogs from "./Dialogs.vue";
import DeezerSlide from "./pitchSlides/DeezerSlide.vue";
import DoubtSlide from "./pitchSlides/DoubtSlide.vue";
import FinalSlide from "./pitchSlides/FinalSlide";
import LyricsSlide from "./pitchSlides/LyricsSlide.vue";
import MashupsSlide from "./pitchSlides/MashupsSlide.vue";
import OrganizationSlide from "./pitchSlides/OrganizationSlide.vue";
import OtherFeatures from "./pitchSlides/OtherFeatures.vue";
import PlaylistsSlide from "./pitchSlides/PlaylistsSlide.vue";
export default {
  data() {
    return {
      currentDialog: 1,
    };
  },
  components: {
    OrganizationSlide,
    Dialogs,
    PlaylistsSlide,
    DoubtSlide,
    LyricsSlide,
    MashupsSlide,
    DeezerSlide,
    OtherFeatures,
    FinalSlide,
  },
  methods: {
    setCurrentDialog(index) {
      this.currentDialog = index;
    },
  },
};
</script>

<style>
.PitchDeck {
  width: 100vw;
  height: 100vh;
}
</style>