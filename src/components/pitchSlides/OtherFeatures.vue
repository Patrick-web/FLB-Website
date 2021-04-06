<template>
  <div class="OtherFeatures">
    <div class="card animated fadeInUp delay-1s">
      <img src="@/assets/images/tag.svg" alt="" />
      <h2>Tag Editor</h2>
    </div>
    <div class="card animated fadeInUp delay-2s">
      <img src="@/assets/images/search.svg" alt="" />
      <h2>Intuitive Search</h2>
    </div>
    <div class="card animated fadeInUp delay-3s">
      <img src="@/assets/images/podcast.svg" alt="" />
      <h2>Podcasts</h2>
      <p>Soon</p>
    </div>
    <div class="card animated fadeInUp delay-4s">
      <img src="@/assets/images/spotify.svg" alt="" />
      <h2>Spotify</h2>
      <p>Soon</p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.OtherFeatures {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  align-items: center;
  gap: 40px;
  padding: 40px;
  height: 85%;
  @media (max-width: 700px) {
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    align-items: flex-start;
    height: 50%;
    transform: translateY(-50px);
    .card {
      height: 140px !important;
      img {
        width: 50px !important;
      }
      h2 {
        font-size: 1rem !important;
      }
      p {
        font-size: 0.5rem !important;
      }
    }
  }
  .card {
    background: var(--accentColor);
    height: 350px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    border-radius: 20px;
    position: relative;
    img {
      width: 130px;
    }
    p {
      position: absolute;
      top: 10px;
      right: 10px;
      background: white;
      color: var(--accentColor);
      padding: 5px;
      padding-right: 8px;
      padding-left: 8px;
      font-family: roboto-thick;
      border-radius: 20px;
    }
  }
}
</style>