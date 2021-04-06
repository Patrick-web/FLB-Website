<template>
  <div class="LyricsSlide singleVideoSlide">
    <div class="card animated fadeInUp delay-1s">
      <video autoplay src="@/assets/videos/lyricsTab.mp4"></video>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.singleVideoSlide {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 85%;
  .card {
    border-radius: 10px;
    width: 80%;
    height: 490px;
    overflow: hidden;
    @media (max-width: 700px) {
      width: 100%;
    }
  }
  video {
    width: 100%;
  }
}
</style>