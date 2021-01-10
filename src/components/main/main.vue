<template>
  <div class="main"
       v-bind:style="{background: color}"
  >
    <div class="main__content" @mousemove="mousemove">
      <div class="main-content__wrapper">
        <div class="main__item">
          <div class="main__color-icon main__color-white-smoke"
               @click="setColor('#F5F5F5')"
          />
          <p class="main__color-title">
            WhiteSmoke #F5F5F5
          </p>
        </div>
        <div class="main__item">
          <div class="main__color-icon main__color-peach-puff"
               @click="setColor('#FFDAB9')"
          />
          <p class="main__color-title">
            PeachPuff #FFDAB9
          </p>
        </div>
        <div class="main__item">
          <div class="main__color-icon main__color-lavender"
               @click="setColor('#E6E6FA')"
          />
          <p class="main__color-title">
            Lavender #E6E6FA
          </p>
        </div>
        <div class="main__item">
          <div class="main__color-icon main__color-light-slate-gray"
               @click="setColor('#778899')"
          />
          <p class="main__color-title">
            LightSlateGray #778899
          </p>
        </div>
        <div class="main__item">
          <div class="main__color-icon main__color-medium-slate-blue"
               @click="setColor('#9370DB')"
          />
          <p class="main__color-title">
            MediumSlateBlue #9370DB
          </p>
        </div>
        <div class="main__item">
          <div class="main__color-icon main__color-light-yellow"
               @click="setColor('#FFFFE0')"
          />
          <p class="main__color-title">
            LightYellow #FFFFE0
          </p>
        </div>
        <div class="main__item">
          <div class="main__color-icon main__color-light-salmon"
               @click="setColor('#FFA07A')"
          />
          <p class="main__color-title">
            LightSalmon #FFA07A
          </p>
        </div>
        <div class="main__item">
          <div class="main__color-icon main__color-honey-dew"
               @click="setColor('#F0FFF0')"
          />
          <p class="main__color-title">
            Honeydew #F0FFF0
          </p>
        </div>
        <div class="main__item">
          <div class="main__color-icon main__color-medium-purple"
               @click="setColor('#9370DB')"
          />
          <p class="main__color-title">
            MediumPurple #9370DB
          </p>
        </div>
        <div class="main__item">
          <div class="main__color-icon main__color-rosy-brown"
               @click="setColor('#FFC1C1')"
          />
          <p class="main__color-title">
            RosyBrown #FFC1C1
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Main",

  data () {
    return {
      color: ''
    }
  },

  methods: {
    setColor (value) {
      this.color = value
    },

    mousemove (e) {
      let mouseX = e.clientX;
      let mouseY = e.clientY;

      let main = document.querySelectorAll('.main');

      for (let i = 0; i < main.length; i++) {
        let nMain = main[i];

        let content = nMain.querySelector('.main__content');

        let content_x = mouseX - this.coords(content).x;
        let content_y = mouseY - this.coords(content).y;
        content.style.transform = `translateY(-${content_y/45}px) translateX(-${content_x/45}px)`
      }
    },

    coords (el) {
      let coords = el.getBoundingClientRect();

      return {
        x: coords.left / 2,
        y: coords.top / 2,
      }
    }
  }
}
</script>

<style scoped lang="scss">
.main {
  background: linear-gradient(to top left, powderblue, pink);
  width: 100%;
  height: 100vh;
  display: flex;

  .main__content {
    max-width: 800px;
    width: 100%;
    height: 450px;
    margin: 0 auto;
    align-self: center;
    display: flex;
    box-shadow: 1px 10px 20px rgba(0, 0, 0, 0.5);
    border-radius: 15px;
    background: rgba(250, 250, 250, 0.1);

    .main-content__wrapper {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      max-width: 750px;
      align-self: center;
      width: 100%;
      max-height: 330px;
      margin: 0 auto;

      .main__item {
        width: 110px;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        margin: 0 40px 40px 0;

        &:nth-child(5) {
          margin: 0 0 40px 0;
        }

        &:nth-child(6) {
          margin: 0 40px 0 0;
        }

        &:nth-child(7) {
          margin: 0 40px 0 0;
        }

        &:nth-child(8) {
          margin: 0 40px 0 0;
        }

        &:nth-child(9) {
          margin: 0 40px 0 0;
        }

        &:nth-child(10) {
          margin: 0 0 0 0;
        }

        .main__color-icon {
          background-color: aqua;
          width: 70%;
          margin: 0 auto 10px;
          height: 75px;
          cursor: pointer;
        }

        .main__color-white-smoke {
          background-color: #f5f5f5;
        }

        .main__color-peach-puff {
          background-color: #ffdab9;
        }

        .main__color-lavender {
          background-color: #e6e6fa;
        }

        .main__color-light-slate-gray {
          background-color: #778899;
        }

        .main__color-medium-slate-blue {
          background-color: #7B68EE;
        }

        .main__color-light-yellow {
          background-color: #ffffe0;
        }

        .main__color-light-salmon {
          background-color: #ffa07a;
        }

        .main__color-honey-dew {
          background-color: #f0fff0;
        }

        .main__color-medium-purple {
          background-color: #9370DB;
        }

        .main__color-rosy-brown {
          background-color: #ffc1c1;
        }

        .main__color-title {
          font-size: 18px;
          font-weight: 300;
        }
      }
    }
  }
}
</style>
