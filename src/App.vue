<template>
    <div id="app">
        <div id="logo"></div>
        <div class="lang-switch">
            <button class="common" @click="lang = 'en'">English</button>
            <button class="common" @click="lang = 'de'">Deutsch</button>
        </div>
        <div class="container" v-if="lang === 'en'">
            <p>Welcome to the first alpha test of Rise in Time.</p>
            <p>This is a very early alpha. A lot of feature are still missing or need improvement.
                But it's important to get early feedback as well as to detect bugs.</p>
            <p>Join the discord channel to stay up to date, talk to other testers, report bugs or suggest features!
                <br><a href="https://discord.gg/xe3452K" target="_blank">https://discord.gg/QpS6PD</a></p>
            <p>Please fill the following survey when you're done with testing:
                <br><a href="https://goo.gl/forms/db1lfJc3eGfBRqs83" target="_blank">https://goo.gl/forms/db1lfJc3eGfBRqs83</a></p>
            <p>The game goal of this alpha round is to reach the victory field on layer 2.
                The player who conquers that field first will get an entry on the 'Board of Immortality'.</p>
            <p>Report bugs and exploits immediately and don't abuse them for your own purpose.</p>
            <p>Thanks for testing and have fun!</p>
        </div>
        <div class="container" v-if="lang === 'de'">
            <p>Willkommen zum ersten Alpha Test von Rise in Time.</p>
            <p>Dies is ein sehr früher Alpha Test. Viele Funktionen fehlen noch oder müssen noch verbessert werden.
                Allerdings ist es sehr wichtig bereits jetzt Rückmeldungen zu bekommen und allfällige Fehler zu
                finden.</p>
            <p>Verbinde dich mit dem Discord Kanal! Dadurch bleibst du informiert, kannst mit anderen Tester sprechen,
                Fehler melden oder neue Funktionen vorschlagen.
                <br><a href="https://discord.gg/QpS6PD" target="_blank">https://discord.gg/QpS6PD</a></p>
            <p>Bitte füllt diese Umfrage aus wenn du fertig bist mit dem Testen:
                <br><a href="https://goo.gl/forms/db1lfJc3eGfBRqs83" target="_blank">https://goo.gl/forms/db1lfJc3eGfBRqs83</a></p>
            <p>Das Ziel dieser Alpha Runde ist es das Siegesfeld auf Ebene 2 zu erreichen.
                Der erste Spieler der dieses Feld erobert bekommt ein Eintrag auf dem 'Board of Immortality'.</p>
            <p>Melde Bugs sofort und nutze sie nicht für deine eigenen Zwecke aus.</p>
            <p>Danke fürs Testen und viel Spass beim Spielen!</p>
        </div>

        <a href="https://riseinti.me">
            <button class="common white play" @click="lang = 'en'">Play!</button>
        </a>
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
        padding: 20px 0;
        font-family: Verdana, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: white;
        min-height: calc(100vh - 40px);
    }

    #logo {
        background: url(./assets/rise_in_time.png) no-repeat;
        background-size: contain;
        width: 613px;
        height: 200px;
        margin: 0 auto;
    }

    @media (max-width: 768px) {
        #logo {
            width: 270px;
            height: 90px;
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

    .play {
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
