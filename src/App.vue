<template>
  <div id="app">
    <div id="logo"></div>
    <div class="lang-switch">
      <button class="common" @click="lang = 'en'">English</button>
      <button class="common" @click="lang = 'de'">Deutsch</button>
    </div>
    <div class="container" v-if="lang === 'en'">
      <p>Welcome to the first alpha test of Rise in Time.</p>
      <p>This is a very early alpha test. A lot of feature are still missing or need improvement.
        But it's important to get early feedback as well as to detect bugs.</p>
      <p>Join the discord channel to stay up to date, talk to other testers, report bugs or suggest features!
      <a href="https://discord.gg/QpS6PD" target="_blank">https://discord.gg/QpS6PD</a></p>
      <p>Please fill the following survey if your done with testing:</p>
      <p>The game goal of this alpha round is to reach the victory field on layer 2.
      The player who conquers that field first will get an entry on the 'Board of Immortality'. </p>
      <p>Thanks for testing and have fun!</p>
    </div>
    <div class="container" v-if="lang === 'de'">
      RIT Alpha Deutsch
    </div>

    <button class="common white play" @click="lang = 'en'">Play!</button>
  </div>
</template>

<script>
    export default {
        name: 'home',
        data() {
            return {
                lang: 'en'
            }
        },
        methods: {},
        beforeMount() {
        }
    }
</script>

<style scoped>
  #app {
    background: url(./assets/background3.png) no-repeat center center fixed;
    background-size: cover;
    padding-top: 20px;
    font-family: Verdana, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: white;
    min-height: calc(100vh - 20px);
  }

  #logo {
    background: url(./assets/rise_in_time.png) no-repeat;
    background-size: contain;
    width: 613px;
    height: 124px;
    margin: 0 auto;
  }
  @media (max-width: 768px){
    #logo {
      width: 270px;
      height: 55px;
    }
  }

  p {
    font-size: 18px;
    font-weight: 500;
    margin: 20px;
    line-height: 22px;
    text-align: left;
  }

  a {
    color: darkblue;
    text-shadow: 0 0 3px white, 0 0 8px white;
  }
  a:hover {
    text-shadow: 0 0 10px white, 0 0 15px white;
  }

  .container {
    max-width: 620px;
    margin: 20px auto;
    padding: 0 10px;
  }

  .play{
    width: 100px;
    font-size: 18px;
  }

  /* BUTTON */
  button.common {
    background-image: url(./assets/button_common.png);
    color: white;
    font-weight: 600;
    text-shadow: 0 0 10px black, 0 0 20px black;
    box-shadow: 0 0 5px 2px black;
    background-size: cover;
    border-radius: 3px;
    padding: 4px;
    border: 0;
    margin: 5px;
  }

  button.common:hover {
    box-shadow: 0 0 5px 2px white;
  }

  button.common.white {
    box-shadow: 0 0 5px 2px white;
  }

  button.common.white:hover {
    box-shadow: 0 0 5px 2px black;
  }
</style>
