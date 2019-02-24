<template>
    <div id="app">
        <div id="logo"></div>
        <div class="lang-switch">
            <button class="common" @click="lang = 'en'">English</button>
            <button class="common" @click="lang = 'de'">Deutsch</button>
        </div>
        <div class="container" v-if="lang === 'en'">
            <p>Welcome to the second alpha test of Rise in Time.</p>
            <p>Join the discord channel to stay up to date, talk to other testers, report bugs or suggest features!
                <br><a href="https://discord.gg/xe3452K" target="_blank">https://discord.gg/QpS6PD</a></p>
            <p>The game goal of this alpha round is to reach the victory field on layer 2.
                The team who conquers that field first will get an entry on the
                <a href="https://boi.riseintime.org" target="_blank">Board of Immortality</a>.</p>
            <p>Report bugs and exploits immediately and don't abuse them for your own purpose.</p>
            <p>This is an open alpha, so feel free to invite your friends.</p>
            <p>Thanks for testing and have fun!</p>
        </div>
        <div class="container" v-if="lang === 'de'">
            <p>Willkommen zum zweiten Alpha Test von Rise in Time.</p>
            <p>Verbinde dich mit dem Discord Kanal! Dadurch bleibst du informiert, kannst mit anderen Tester sprechen,
                Fehler melden oder neue Funktionen vorschlagen.
                <br><a href="https://discord.gg/QpS6PD" target="_blank">https://discord.gg/QpS6PD</a></p>
            <p>Das Ziel dieser Alpha Runde ist es das Siegesfeld auf Ebene 2 zu erreichen.
                Das erste Team das dieses Feld erobert bekommt ein Eintrag auf dem
                <a href="https://boi.riseintime.org" target="_blank">Board of Immortality</a>.</p>
            <p>Melde Bugs sofort und nutze sie nicht für deine eigenen Zwecke aus.</p>
            <p>Dies ist eine offener Alpha Test, lade deine Freunde ein.</p>
            <p>Danke fürs Testen und viel Spass beim Spielen!</p>
        </div>

        <a href="https://play.google.com/store/apps/details?id=org.riseintime.riseintime">
            <button class="common play" @click="lang = 'en'">Dowload app</button>
        </a><br/>
        <a href="https://riseintime.org">
            <button class="common play" @click="lang = 'en'">Play in browser</button>
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

    .red {
        color: red;
        font-weight: bold;
    }

    .container {
        max-width: 620px;
        margin: 20px auto;
        padding: 0 10px;
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
        margin: 10px;
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

    .play {
        width: 150px;
        font-size: 14px;
    }
</style>
