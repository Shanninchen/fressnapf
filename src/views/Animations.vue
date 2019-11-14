<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <v-flex
        xs12
        mb-5
      >
    <h1>Animations</h1>
    <p class="subheading font-weight-bold mb-3">
      Leider sind viele Animation für die iPad Nutzung angelegt worden,
      deswegen sollte man sich diese Seite auf einem Desktop Rechner anschauen.
    </p>
        <v-carousel
          dark
          height="768">
          <v-carousel-item
          >
            <div class="animation-container">
              <div class="animate-btn-container">
                <v-btn
                  depressed
                  large
                  @click="removeAnimationPause"
                  light
                  ripple
                  id="animation-btn1"
                >
                  Animieren
                </v-btn>
              </div>
              <img src="../assets/device@2x.png" class="device">
              <img src="../assets/device-head@2x.png" class="device-head">
              <img src="../assets/smoke@2x.png" class="smoke animation-paused">
            </div>
          </v-carousel-item>
          <v-carousel-item
          >
            <div class="animation-container">
              <div class="animate-btn-container">
                <v-btn
                  depressed
                  large
                  @click="addBarAnimation"
                  light
                  ripple
                  id="animation-btn2"
                >
                  Animieren
                </v-btn>
              </div>
              <img src="../assets/background@2x.jpg" class="slide-background">
              <div class="animation-bar-container">
                <img src="../assets/bars@2x.png" class="bars">
              </div>
            </div>
          </v-carousel-item>
        </v-carousel>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
export default {
  name: 'Animations',
  methods: {
    removeAnimationPause() {
      document.getElementsByClassName('smoke')[0].classList.remove('animation-paused');
      document.getElementById('animation-btn1').classList.add('v-btn--disabled');
    },
    addBarAnimation() {
      document.getElementsByClassName('animation-bar-container')[0].classList.add('animated');
      document.getElementById('animation-btn1').classList.add('v-btn--disabled');
    },
  },
};
</script>
<style lang="scss">
  .animation-container {
    background-color: #4c4a4a;
    width: 100%;
    height: 768px;
  }

  .device-head {
    position: absolute;
    width: 81px;
    left: 800px;
    top: 426px;
    transform: rotate(2deg);
    z-index: 1;
  }

  .device {
    position: absolute;
    width: 287px;
    left: 766px;
    top: 428px;
    z-index: 3;
    transform: rotate(2deg);
  }

  .smoke {
    position: absolute;
    opacity: 0;
    animation: smoke-animation 2s .5s forwards;
    z-index: 2;
    width: 681px;
    left: 262px;
    top: -8px;
    pointer-events: none;
  }

  .animation-paused {
    animation-play-state: paused;
  }

  .slide-background {
    width: 1024px;
    height: 768px;
  }

  .animate-btn-container {
    z-index: 100;

    .v-btn {
      margin-top: 40px;
      margin-bottom: 20px;
    }
  }

  .animation-bar-container {
    position: absolute;
    width: 0;
    height: 313px;
    top: 370px;
    left: 214px;
    overflow: hidden;
    transition: width 1s ease-in;

    img {
      width: 489px;
      display: block;
    }

    &.animated {
      width: 498px;
    }
  }

  @keyframes smoke-animation {
    0% {
      opacity: 0;
      transform: scale3d(0,0,0);
      transform-origin: 100% 100%;
    }

    100% {
      opacity: 1;
      transform: scale3d(1,1,1);
      transform-origin: 100% 100%;
    }
  }
</style>
