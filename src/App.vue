<template>
  <div id="app">
    <div class="landing">
      <h1 class="hidden">FLB Music</h1>
      <div class="animated fadeInUp" id="headingTitle">
        <div class="heading">
          <img src="@/assets/images/FLB Double Logo.svg" alt="" />
          <h1>LB Music</h1>
        </div>
        <h3>
          The
          <span id="nextText"
            >Next <img id="nextArrow" src="@/assets/images/arrow.svg" alt="" />
          </span>
          big💣 thing,
        </h3>
        <h4>In Music 🎶 though</h4>
      </div>
    </div>
    <div class="previews">
      <Previews />
    </div>
    <a
      class="downloadButton"
      href="https://github.com/Patrick-web/FLB-Music-Player-Official/releases/download/v1.0.4/FLB-Music-Setup-1.0.4.exe"
    >
      <img src="@/assets/images/windows.svg" alt="" />
      <p>Download</p>
    </a>
  </div>
</template>

<script>
import Previews from "./components/Previews.vue";
export default {
  name: "App",
  components: { Previews },
};
</script>

<style lang="scss">
@import "./assets/css/global.css";
@import "./assets/css/animate.css";

#app {
  height: 100vh;
  width: 100vw;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  background: linear-gradient(306deg, #284854, #492e35) !important;
  transition: 0.2s ease;
  display: grid;
  grid-template-columns: 2fr 3fr;
  @media (max-width: 700px) {
    display: flex;
    flex-direction: column;
  }
}
.hidden {
  display: none;
}
#headingTitle {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  .heading {
    padding: 5px;
    display: flex;
    align-items: baseline;
    justify-content: center;
    margin-top: 10px;
    img {
      width: 5rem;
    }
    h1 {
      font-size: 5rem;
      font-family: roboto-thick;
      transform: translateY(-10px) translateX(-10px);
      text-shadow: 2.5px 2.5px rgba(255, 255, 255, 0.219);
    }
    @media (max-width: 700px) {
      img {
        width: 3rem;
      }
      h1 {
        font-size: 3rem;
      }
    }
  }
  @media (max-width: 700px) {
    align-items: center;
  }
}

#nextText {
  position: relative;
}
#nextArrow {
  position: absolute;
  width: 50px;
  right: 0px;
  top: 0px;
  transform: translateY(-80%) translateX(80%);
}

.landing {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  h3,
  h4 {
    text-align: left;
    font-weight: 300;
  }
  h3 {
    font-size: 2rem;
  }
  h4 {
    font-size: 1.3rem;
    font-family: roboto-thin;
  }
  @media (max-width: 700px) {
    margin-bottom: 20px;
    h4 {
      font-size: 1.1rem;
    }
    h3 {
      font-size: 1.2rem;
    }
  }
}
.downloadButton {
  margin: auto;
  margin-top: 40px;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  background: white;
  padding: 10px;
  padding-right: 20px;
  padding-left: 20px;
  border-radius: 2rem;
  position: fixed;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  transition: 0.2s ease-in-out;
  p {
    color: var(--accentColor);
    font-family: roboto-thick;
    font-size: 2rem;
  }
  img {
    width: 1.5rem;
    margin-right: 10px;
  }
  &:hover {
    border-radius: 1rem;
  }
  @media (max-width: 700px) {
    p {
      font-size: 1.2rem;
      img {
        width: 1rem;
      }
    }
  }
}
.previews {
  display: flex;
  align-items: center;
  justify-content: center;
  @media (max-width: 700px) {
    height: 60%;
  }
}
</style>
