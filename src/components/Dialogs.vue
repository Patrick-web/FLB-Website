<template>
  <div id="Dialogs" class="dialog_1">
    <p>My Child, why have doubt in the prophesy😞</p>
    <p>Look how beautifully🌹 I'll your organize music by</p>
    <p>And how neatly👔 I'll stack your playlists</p>
    <p>I'll even show you the lyrics📜 to that song your fumbling about</p>
    <p>When your bored, I'll dose you with daily mashups 🎉</p>
    <p>And when you've exhausted all your local music😖</p>
    <p>And many other features</p>
    <p>All this...</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentDialog: 1,
    };
  },
  mounted() {
    const dialogsWrapper = document.querySelector("#Dialogs");
    setTimeout(() => {
      dialogsWrapper.classList.replace("dialog_1", `dialog_2`);
      this.currentDialog = 2;
      this.$emit("currentDialog", this.currentDialog);
    }, 5000);
    setInterval(() => {
      if (this.currentDialog <= 7) {
        this.currentDialog += 1;
        const currentClass = dialogsWrapper.getAttribute("class");
        dialogsWrapper.classList.replace(
          currentClass,
          `dialog_${this.currentDialog}`
        );
        document.body.querySelector(
          "#app"
        ).className = `active_class_${this.currentDialog}`;
        this.$emit("currentDialog", this.currentDialog);
      } else {
        window.clearInterval();
      }
    }, 12000);
  },
};
</script>

<style lang="scss">
#Dialogs {
  height: 100px;
  position: relative;
  @media (max-width: 700px) {
    transform: translateX(-20px) scale(0.8);
  }
  p {
    font-family: roboto-light;
    font-size: 1.2rem;
    position: absolute;
    left: 35px;
    top: 70px;
    transition: 1s;
    opacity: 0;
  }
}
.dialog_1 p:first-child {
  top: 50px !important;
  left: 40px !important;
  opacity: 1 !important;
}
.dialog_1 p:not(:first-child) {
  opacity: 0;
}

.dialog_2 p:nth-child(2) {
  top: 50px !important;
  left: 40px !important;
  opacity: 1 !important;
}
.dialog_2 p:not(:nth-child(2)) {
  opacity: 0;
}
.dialog_2 p:first-child {
  opacity: 0.2 !important;
  font-size: 1rem !important;
  top: 10px !important;
  /* left: 35px !important; */
}

.dialog_3 p:nth-child(3) {
  top: 50px !important;
  left: 40px !important;
  opacity: 1 !important;
}
.dialog_3 p:first-child {
  top: 0px !important;
  left: 25px !important;
  opacity: 0;
  font-size: 0.8rem !important;
}
.dialog_3 p:nth-child(2) {
  opacity: 0.2 !important;
  font-size: 1rem !important;
  top: 10px !important;
  /* left: 35px !important; */
}

.dialog_4 p:nth-child(4) {
  top: 50px !important;
  left: 40px !important;
  opacity: 1 !important;
}
.dialog_4 p:nth-child(2) {
  top: 0px !important;
  left: 25px !important;
  opacity: 0;
  font-size: 0.8rem !important;
}
.dialog_4 p:nth-child(3) {
  opacity: 0.2 !important;
  font-size: 1rem !important;
  top: 10px !important;
  /* left: 35px !important; */
}

.dialog_5 p:nth-child(5) {
  top: 50px !important;
  left: 40px !important;
  opacity: 1 !important;
}
.dialog_5 p:nth-child(3) {
  top: 0px !important;
  left: 25px !important;
  opacity: 0;
  font-size: 0.8rem !important;
}
.dialog_5 p:nth-child(4) {
  opacity: 0.2 !important;
  font-size: 1rem !important;
  top: 10px !important;
  /* left: 35px !important; */
}

.dialog_6 p:nth-child(6) {
  top: 50px !important;
  left: 40px !important;
  opacity: 1 !important;
}
.dialog_6 p:nth-child(4) {
  top: 0px !important;
  left: 25px !important;
  opacity: 0;
  font-size: 0.8rem !important;
}
.dialog_6 p:nth-child(5) {
  opacity: 0.2 !important;
  font-size: 1rem !important;
  top: 10px !important;
  /* left: 35px !important; */
}

.dialog_7 p:nth-child(7) {
  top: 50px !important;
  left: 40px !important;
  opacity: 1 !important;
}
.dialog_7 p:nth-child(5) {
  top: 0px !important;
  left: 25px !important;
  opacity: 0;
  font-size: 0.8rem !important;
}
.dialog_7 p:nth-child(6) {
  opacity: 0.2 !important;
  font-size: 1rem !important;
  top: 10px !important;
  /* left: 35px !important; */
}

.dialog_8 p:nth-child(8) {
  top: 50px !important;
  left: 40px !important;
  opacity: 1 !important;
}
.dialog_8 p:nth-child(6) {
  top: 0px !important;
  left: 25px !important;
  opacity: 0;
  font-size: 0.8rem !important;
}
.dialog_8 p:nth-child(7) {
  opacity: 0.2 !important;
  font-size: 1rem !important;
  top: 10px !important;
  /* left: 35px !important; */
}
</style>