<template>
  <section class="container">
    <div class="line-one"></div>
    <div class="line-two"></div>
    <div class="title-container">
      <h1>コミックマーケット94 西め07a</h1>
      <h2>お気持ち虚無同盟</h2>
    </div>
    <div class="block-container">
      <div>
        <div class="hexagon himanoa">
          <div class="hexagon-inner-1">
            <div class="hexagon-inner-2">
              <div class="hexagon-inner-3">
                <div class="hexagon-inner-black">
                  <div class="himanoa-content">
                    <h3>Discordで動く<br />Vtuber生放送<br />通知Bot</h3>
                    <div class="name-image">
                      <p>himanoa</p>
                      <img src="~/assets/himanoa.png">
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="hexagon masaaki">
          <div class="hexagon-inner-1">
            <div class="hexagon-inner-2">
              <div class="hexagon-inner-3">
                <div class="hexagon-inner-black">
                  <div class="masaaki-content">
                    <h3>Vuexのいろは</h3>
                    <div class="name-image">
                      <p>masaaki</p>
                      <img src="~/assets/masaaki.png">
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="hexagon nametake">
          <div class="hexagon-inner-1">
            <div class="hexagon-inner-2">
              <div class="hexagon-inner-3">
                <div class="hexagon-inner-black">
                  <div class="nametake-content">
                    <h3>大学を<br />無事卒業しよう</h3>
                    <div class="name-image">
                      <p>nametake</p>
                      <img src="~/assets/nametake.png">
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="hexagon potato">
          <div class="hexagon-inner-1">
            <div class="hexagon-inner-2">
              <div class="hexagon-inner-3">
                <div class="hexagon-inner-black">
                  <div class="potato-content">
                    <h3>技術同人誌の<br />デザインと執筆環境</h3>
                    <div class="name-image">
                      <p>potato4d</p>
                      <img src="~/assets/potato.png">
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <el-button  @click="dialogVisible = true">おしながき</el-button>
    <el-dialog
      :visible.sync="dialogVisible"
      width="70%"
      center>
      <img src="~/assets/oshina.png" class="oshinagki">
    </el-dialog>
    <AppCharacter />
  </section>
</template>

<script>
import AppCharacter from '~/components/AppCharacter.vue'

export default {
  components: {
    AppCharacter
  },
  data () {
    return {
      dialogVisible: false
    }
  }
}
</script>

<style scoped lang="scss">
.container {
  min-height: 100vh;
  max-width: 100%;
  position: relative;
  overflow: hidden;
}

.line-one {
  background-color: #D54D4D;
  width: 0; height: 220px;
  position: absolute;
  top: 75px; left: -40px;
  transform: rotate(-10deg);
  animation: lineFadeIn 1.5s ease 0s forwards;
}

.line-two {
  background-color: #c74848;
  width: 0; height: 280px;
  position: absolute;
  left: -130px; bottom: 100px;
  transform: rotate(20deg);
  animation: lineFadeIn 1.5s ease 1s forwards;
}

@keyframes lineFadeIn {
  0% {
    width: 0;
  }
  100% {
    width: 120vw;
  }
}

.title-container {
  background-color: #4A1B1B;
  padding: 15px 15px 15px 50px;
  position: absolute;
  animation: titleFadeIn 1s ease 2s forwards;
  opacity: 0;
  width: 0; height: 130px;

  @keyframes titleFadeIn {
    0% {
      width: 0;
      opacity: 0;
    }
    100% {
      width: 100%;
      opacity: 1;
    }
  }

  h1, h2 {
    color: #fff;
    line-height: 1;
    opacity: 0;
    animation: titleTextFadeIn 1s ease 3s forwards;

    @keyframes titleTextFadeIn {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }
  }

  h1 {
    font-size: 45px;
    margin-bottom: 15px;
  }

  h2 {
    font-size: 32px;
  }
}

.block-container {
  position: absolute;
  top: 300px; left: 50px;
  width: 500px; height: 500px;

  & > div {
    position: relative;
    display: flex;
    flex-flow: wrap;

    .hexagon {
      position: relative;
      width: 220px;
      overflow: hidden;
      &::before {
        display: block;
        padding-top: 86.602540378%;
        content: '';
      }
    }
    .hexagon-inner-1 {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      overflow: hidden;
      transform: rotate(60deg);
    }
    .hexagon-inner-2 {
      width: 100%; height: 100%;
      overflow: hidden;
      transform: rotate(60deg);
    }
    .hexagon-inner-3 {
      width: 100%; height: 100%;
      transform: rotate(-120deg);
    }

    .hexagon-inner-black {
      width: 100%; height: 100%;
      background-color: #551f1f;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
    }
  }
}

.himanoa {
  opacity: 0;
  animation: otakuHexagonFadeIn 1s ease 4s forwards;

  @keyframes otakuHexagonFadeIn {
    0% {
      opacity: 0;
      transform: rotate(1080deg) scale(0);
    }
    100% {
      opacity: 1;
    }
  }

  .himanoa-content {
    text-align: center;
    color: #fff;
    animation: otakuText .5s ease 5.5s forwards;
    opacity: 0;

    .name-image {
      display: flex;
      align-items: center;
      position: absolute;
      justify-content: space-between;
      width: 120px;
      bottom: 10px;
      left: calc(50% - 60px);

      p {
        font-weight: bold;
        font-size: 15px;
      }

      img {
        width: 40px;
        height: 40px;
        display: block;
      }
    }
  }
}

.masaaki {
  left: -35px;
  top: 105px;
  opacity: 0;
  animation: otakuHexagonFadeIn 1s ease 4.5s forwards;

  .masaaki-content {
    text-align: center;
    color: #fff;
    animation: otakuText .5s ease 5.5s forwards;
    opacity: 0;

    .name-image {
      display: flex;
      align-items: center;
      position: absolute;
      justify-content: space-between;
      width: 120px;
      bottom: 10px;
      left: calc(50% - 60px);

      p {
        font-weight: bold;
        font-size: 15px;
      }

      img {
        width: 40px;
        height: 40px;
        display: block;
      }
    }
  }
}

.potato {
  left: -35px;
  top: 130px;
  animation: otakuHexagonFadeIn 1s ease 5.5s forwards;
  opacity: 0;
  .potato-content {
    text-align: center;
    color: #fff;
    animation: otakuText .5s ease 6.5s forwards;
    opacity: 0;

    .name-image {
      display: flex;
      align-items: center;
      position: absolute;
      justify-content: space-between;
      width: 120px;
      bottom: 10px;
      left: calc(50% - 60px);

      p {
        font-weight: bold;
        font-size: 15px;
      }

      img {
        width: 40px;
        height: 40px;
        display: block;
      }
    }
  }
}

.nametake {
  top: 25px;
  opacity: 0;
  animation: otakuHexagonFadeIn 1s ease 5s forwards;

  .nametake-content {
    text-align: center;
    color: #fff;
    animation: otakuText .5s ease 6s forwards;
    opacity: 0;

    .name-image {
      display: flex;
      align-items: center;
      position: absolute;
      justify-content: space-between;
      width: 120px;
      bottom: 10px;
      left: calc(50% - 60px);

      p {
        font-weight: bold;
        font-size: 15px;
      }

      img {
        width: 40px;
        height: 40px;
        display: block;
      }
    }
  }
}

@keyframes otakuHexagonFadeIn {
  0% {
    opacity: 0;
    transform: rotate(1080deg) scale(0);
  }
  100% {
    opacity: 1;
  }
}

@keyframes otakuText {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.el-button {
  position: absolute;
  bottom: 60px; left: 50px;
  background: #551f1f !important;
  color: #fff !important;
  z-index: 1000;
  font-weight: bold;
  font-size: 18px;
  animation: modalBtn .3s ease 6.5s forwards !important;
  opacity: 0;
}

@keyframes modalBtn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.oshinagki {
  width: 100%;
  height: 100%;
}
</style>
