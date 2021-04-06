<template>
  <div class="orgSlide">
    <div class="card card animated fadeInUp delay-1s">
      <h3>🎭 Artists</h3>
      <div class="videoWrapper">
        <video autoplay src="@/assets/videos/Artiststab.mp4"></video>
      </div>
    </div>
    <div class="card card animated fadeInUp delay-2s">
      <h3>📕 Albums</h3>
      <div class="videoWrapper">
        <video autoplay src="@/assets/videos/Albumstab.mp4"></video>
      </div>
    </div>
    <div class="card animated fadeInUp delay-3s">
      <h3>and even Folders 📂</h3>
      <div class="videoWrapper">
        <video autoplay src="@/assets/videos/Folderstab.mp4"></video>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.orgSlide {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  padding: 40px;
  .card {
    h3 {
      text-align: left;
      margin-bottom: 20px;
      font-size: 1.3rem;
    }
    .videoWrapper {
      height: 280px;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      position: relative;
      overflow: hidden;
      border-radius: 10px;
      video {
        position: absolute;
        width: 160%;
        right: 0px;
        transform: translateX(22.7%) translateY(-20px);
      }
    }
  }
}
</style>