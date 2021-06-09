<template>
  <div id="app">
    <vue-particles :clickEffect="false" color="#dedede"></vue-particles>
    <img src="@/assets/images/artists up-min.png" id="l_bg" alt="" />
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
    <div class="flex downloadWrapper">
      <h3>Download</h3>
      <div class="btns">
        <a
          href="https://github.com/Patrick-web/FLB-Music-Player-Official/releases/download/v1.1.0/FLB-Music-Setup-1.1.0.exe"
        >
          <img src="@/assets/images/windows.svg" alt="" />
          <p>Windows</p>
        </a>
        <a
          href="https://github.com/Patrick-web/FLB-Music-Player-Official/releases/download/v1.1.0/FLB-Music-1.1.0.AppImage"
        >
          <img src="@/assets/images/linux.svg" alt="" />
          <p>Linux</p>
        </a>
      </div>
    </div>
    <Fsection />
  </div>
</template>

<script>
import Fsection from "./components/Fsection.vue";
export default {
  name: "App",
  components: { Fsection },
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
  background: rgb(0, 0, 15);
  transition: 0.2s ease;
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
  justify-content: left;
  padding-left: 40px;
  align-items: center;
  height: 100vh;
  position: relative;
  z-index: 5;
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
.downloadWrapper {
  background: rgba(255, 255, 255, 0.137);
  backdrop-filter: blur(10px);
  position: fixed;
  transform: translateX(-50%);
  bottom: 20px;
  left: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 10px;
  border-radius: 20px;
  gap: 10px;
  h3 {
    font-size: 2rem;
  }
  .btns {
    gap: 10px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  a {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    background: white;
    padding: 5px 15px;
    border-radius: 2rem;
    transition: 0.2s ease-in-out;
    p {
      color: var(--accentColor);
      font-family: roboto-thick;
      font-size: 1.4rem;
    }
    img {
      width: 1.5rem;
      margin-right: 10px;
    }
    &:hover {
      border-radius: 1rem;
    }
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
#particles-js {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}
#l_bg {
  position: fixed;
  top: 0;
  width: 80%;
  top: 50%;
  filter: brightness(0.8);
  right: 0%;
  transform: translateX(50px) translateY(-50%);
}
</style>
