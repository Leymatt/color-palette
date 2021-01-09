<template>
  <div class="main"
       v-bind:style="{background: color}"
  >
      <div class="main__content">
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
    margin: 0 auto;
    align-self: center;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;


    .main__item {
      width: 110px;
      border-radius: 5px;
      display: flex;
      flex-direction: column;
      margin: 0 60px 40px 0;

      &:nth-child(5) {
        margin: 0 0 40px 0;
      }

      &:nth-child(6) {
        margin: 0 60px 0 0;
      }

      &:nth-child(7) {
        margin: 0 60px 0 0;
      }

      &:nth-child(8) {
        margin: 0 60px 0 0;
      }

      &:nth-child(9) {
        margin: 0 60px 0 0;
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
</style>
