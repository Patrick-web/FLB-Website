<template>
  <div class="preview">
    <img id="laptop" src="@/assets/images/laptop.png" alt="" />
    <img
      v-if="currentPreview == 0"
      class="previewImg"
      src="@/assets/images/hometab.png"
      alt=""
    />
    <img
      v-if="currentPreview == 1"
      class="previewImg"
      src="@/assets/images/albumsTab.png"
      alt=""
    />
    <img
      v-if="currentPreview == 2"
      class="previewImg"
      src="@/assets/images/artistTab.png"
      alt=""
    />
    <img
      v-if="currentPreview == 3"
      class="previewImg"
      src="@/assets/images/playlistTab.png"
      alt=""
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
    }, 2000);
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
  }
  @media (max-width: 700px) {
    width: 90vw;
    .previewImg {
      margin-top: 0px;
    }
  }
}
</style>