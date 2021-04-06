<template>
  <div class="preview">
    <img id="laptop" src="@/assets/images/laptop.png" alt="" />
    <img
      :class="[currentPreview == 0 ? 'visible' : '', 'previewImg']"
      src="@/assets/images/hometab.png"
      alt="Home Tab"
    />
    <img
      :class="[currentPreview == 1 ? 'visible' : '', 'previewImg']"
      src="@/assets/images/albumsTab.png"
      alt="Albums Tab"
    />
    <img
      :class="[currentPreview == 2 ? 'visible' : '', 'previewImg']"
      src="@/assets/images/artistTab.png"
      alt="Artist Tab"
    />
    <img
      :class="[currentPreview == 3 ? 'visible' : '', 'previewImg']"
      src="@/assets/images/playlistTab.png"
      alt="Playlist Tab"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentPreview: 0,
    };
  },
  mounted() {
    setInterval(() => {
      if (this.currentPreview == 3) {
        this.currentPreview = 0;
      } else {
        this.currentPreview += 1;
      }
    }, 3000);
  },
};
</script>

<style lang="scss">
.preview {
  position: relative;
  width: 50vw;
  #laptop {
    width: 100%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .previewImg {
    position: relative;
    z-index: 3;
    width: 77%;
    margin-top: -15px;
    opacity: 0;
    display: none;
    transition: 0.4s opacity;
  }
  .visible {
    opacity: 1;
    display: initial;
  }
  @media (max-width: 700px) {
    width: 90vw;
    .previewImg {
      margin-top: 0px;
    }
  }
}
</style>