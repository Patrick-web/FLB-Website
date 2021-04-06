<template>
  <div id="app">
    <div v-if="!showPitchDeck" class="landing">
      <div class="logoWrapper animated zoomIn">
        <img id="logo" src="@/assets/images/FLB logo.svg" alt="" />
      </div>
      <h1 class="hidden">FLB Music</h1>
      <div class="animated fadeInUp" id="headingTitle">
        <img src="@/assets/images/FLB Double Logo.svg" alt="" />
        <h1>LB Music</h1>
      </div>
      <div class="subHeading animated fadeInUp delay-1s">
        <h3>
          The
          <span id="nextText"
            >Next <img id="nextArrow" src="@/assets/images/arrow.svg" alt="" />
          </span>
          big💣 thing,
        </h3>
        <h4>In Music 🎶 though</h4>
      </div>
      <div class="firstPreviewWrapper">
        <img
          id="firstPreview"
          class="animated fadeInUp delay-1s"
          src="@/assets/images/flb promo.png"
          alt="FLB Preview"
        />
      </div>

      <div class="bottomContent">
        <a
          class="downloadButton animated fadeInUp delay-1s"
          title="Download FLB Music"
          href="https://github.com/Patrick-web/FLB-Music-Player-Official/releases/download/v1.0.0/FLB-Music-Setup-1.0.0.exe"
        >
          <img src="@/assets/images/windows.svg" alt="" />
          <p>Download</p>
        </a>
      </div>
    </div>
    <button
      @click="showPitchDeck = true"
      id="doubt"
      class="animated fadeInUp delay-2s"
      v-if="!showPitchDeck"
    >
      <p>Naah, I don't believe you</p>
    </button>
    <button
      id="believe"
      class="animated tada delay-10s"
      v-if="showPitchDeck"
      @click="showPitchDeck = false"
    >
      Close
    </button>

    <transition enter-active-class="animated fadeInUp">
      <pitch-deck v-if="showPitchDeck" />
    </transition>
  </div>
</template>

<script>
import PitchDeck from "./components/PitchDeck.vue";
export default {
  name: "App",
  data() {
    return {
      showPitchDeck: false,
    };
  },
  components: { PitchDeck },
};
</script>

<style lang="scss">
@import "./assets/css/global.css";
@import "./assets/css/animate.css";

#app {
  height: 100vh;
  width: 100vw;
  overflow: hidden;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  background: linear-gradient(45deg, #503d26, #472c1f, #403131);
  transition: 0.2s ease;
  @media (max-width: 700px) {
    overflow-y: scroll;
  }
}
.logoWrapper {
  margin: auto;
  margin-top: 20px;
  margin-bottom: 20px;
  background: white;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  place-items: center;
  display: none;
  @media (min-width: 700px) {
    display: grid;
    position: fixed;
    top: 20px;
    left: 20px;
    margin: 0px;
  }
  #logo {
    width: 30px;
    height: 30px;
  }
}
.hidden {
  display: none;
}
#headingTitle {
  padding: 5px;
  display: flex;
  align-items: baseline;
  justify-content: center;
  margin-top: 10px;
  img {
    width: 2.5rem;
    margin-left: 5px;
  }
  h1 {
    font-size: 2.5rem;
    font-family: roboto-thick;
    transform: translateY(-10px) translateX(-10px);
    text-shadow: 2.5px 2.5px rgba(255, 255, 255, 0.219);
  }
  @media (min-width: 700px) {
    position: absolute;
    top: 30%;
    left: 40px;
    z-index: 2;
    margin-top: 0px;
    h1 {
      font-size: 6rem;
    }
    img {
      width: 70px;
    }
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

.subHeading {
  margin-left: 40px;
  margin-top: 10px;
  h3 {
    font-size: 1.1rem;
  }
  h3,
  h4 {
    text-align: left;
    font-weight: 400;
  }
  h4 {
    font-family: "Handlee", cursive;
  }
  @media (min-width: 700px) {
    position: absolute;
    top: 58%;
    left: 40px;
    transform: translateY(-50%);
    z-index: 2;
    margin: 0px;
    h3 {
      font-size: 1.8rem;
    }
    h4 {
      font-size: 1.4rem;
    }
  }
}
#firstPreview {
  margin-top: 20px;
  width: 100vw;
  @media (min-width: 700px) {
    position: absolute;
    top: 10%;
    height: 65%;
    width: auto;
    margin: 0px;
    right: 20px;
  }
}

.bottomContent {
  position: absolute;
  bottom: 20px;
  @media (min-width: 700px) {
    left: 50%;
    transform: translateX(-50%);
  }
}
.mobileUsersMsg {
  margin-top: 10px;
  p {
    text-align: left;
    margin-left: 40px;
    font-family: roboto-light;
    font-size: 1.2rem;
    margin-top: 10px;
  }
  @media (min-width: 700px) {
    display: none;
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
  border-radius: 15px;
  position: fixed;
  bottom: 10px;
  left: 10px;
  transition: 0.2s ease-in-out;
  p {
    color: var(--accentColor);
    font-family: roboto-thick;
    font-size: 1rem;
  }
  img {
    width: 15px;
    margin-right: 10px;
  }
  &:hover {
    border-radius: 30px;
  }
  @media (min-width: 700px) {
    width: 200px;
    p {
      font-size: 1.6rem;
    }
    img {
      width: 25px;
    }
  }
}
#doubt {
  background: rgba(255, 255, 255, 0.26);
  padding: 8px;
  border-radius: 10px;
  position: fixed;
  bottom: 15px;
  right: 10px;
  p {
    font-family: roboto-light;
  }
  img {
    width: 100px;
    opacity: 0;
    transform: translateY(20px);
    transition: 0.2s ease;
  }
  &:hover {
    img {
      opacity: 1;
      transform: translateY(0px);
    }
  }
  @media (min-width: 700px) {
    right: 40px;
    bottom: 30px;
    font-size: 1.4rem;
    width: 300px;
  }
}
#believe {
  position: fixed;
  top: 10px;
  right: 40px;
  z-index: 3;
  background: rgba(255, 255, 255, 0.363);
  padding: 8px;
  padding-right: 10px;
  padding-left: 10px;
  color: white;
  backdrop-filter: blur(10px);
  border-radius: 20px;
  transition: 0.2s ease;
  @media (max-width: 700px) {
    top: initial;
    bottom: 20px;
    right: initial;
    left: 40%;
    transform: translateX(-50%);
  }
  &:hover {
    background: var(--accentColor);
    color: white;
    border-radius: 10px;
  }
}
</style>
