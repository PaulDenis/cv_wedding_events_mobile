!<template>
    <div class="landing_page">
        <!-- i componenti di fontawesome crea problemi, mettere l'evento su un componente div. -->
        <div class="container_lingue">
            <div class="lingue" v-on:click="lingua = 'italiano', $emit('lingua', lingua)">
                <img src="../assets/bandiere/it.svg" alt="bandiera italia" title="Lingua italiana">
            </div>
            <div class="lingue" v-on:click="lingua = 'inglese', $emit('lingua', lingua)">
                <img src="../assets/bandiere/us.svg" alt="bandiera america" title="English lenguage">
            </div>
        </div>
        <img src="../assets/banner_background_2.jpg" alt="" class="ladning_background">

        <!-- Versione italiana -->
        <div v-show="lingua == 'italiano'" class="center">
            <h1>CV <span class="block">WEDDINGS <span class="gold">&</span> EVENTS</span></h1>
            <p>I tuoi eventi, quando e come li vuoi</p>
        </div>
                <div class="scroll" v-show="lingua == 'italiano'">
            <h1>Scorri verso il basso <i class="fas fa-chevron-circle-down"></i></h1>
        </div>

        <!-- Versione inglese -->
        <div v-show="lingua == 'inglese'" class="center">
            <h1>CV <span class="block">WEDDINGS <span class="gold">&</span> EVENTS</span></h1>
            <p>Your events, when and how you want them</p>
        </div>
        <div class="scroll" v-show="lingua == 'inglese'">
            <h1>Scroll down <i class="fas fa-chevron-circle-down"></i></h1>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            lingua:"italiano"
        }
    },
    methods: {
        Lingua(lng) {
            this.lingua = lng;
        }
    }
}
</script>

<style lang="scss" scoped>

    .ladning_background {
        height: 100vh;
        position: relative;
        bottom: 20%;
    }
    .container_lingue {
        float: right;
        position: relative;
        z-index: 2;
        background-color: rgba(256, 256, 256, 0.7);
        &::after {
            content: "";
            display: table;
            clear: both;
        }
    }
    .lingue {
        position: relative;
        width: 20px;
        margin: 10px;
        z-index: 2;
        i {
            margin: 10px;
        }
        &:hover {
            cursor: pointer;
        }

    }
    .landing_page {
        position: relative;
        width: 100%;
        height: 95vh;
        overflow: hidden;
    }
    .center {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -90%);
        width: 90%;
        padding: 15px 10px;
        border-radius: 10px;
        text-align: center;
        color: #feb5af;
        background-color: rgba(256, 256, 256, 0.7);
        h1 {
            font-size: 30px;
            .gold {
                color: #bc8d34;
            } 
        text-shadow: 2px 2px 5px black;

        }
        p {
            font-size: 18px;
            color: #bc8d34;
        }
        .block {
            display: block;
        }
        &:hover {
            cursor: pointer;
            background-color: rgba(256, 256, 256, 1);
        }
    }
    .scroll {
        position: absolute;
        bottom: 5%;
        left: 50%;
        transform: translateX(-50%);
        z-index: 2;
        color: white;
        h1 {
            display: inline-block;
            position: relative;
            left: 50%;
            transform: translateX(-50%);
            text-shadow: 1px 1px 3px black;
            font-size: 20px;
            .fa-chevron-circle-down {
                // color: #bc8d34;
                filter: drop-shadow(0px 0px 2px black);
                animation: up_and_down 2s infinite;
            }
        }
        animation: fade_in 4s;
    }

    @keyframes up_and_down {
        0% {
            transform: translateY(0px);
        }
        50% {
            transform: translateY(5px);
        }
        100% {
            transform: translateY(0px);
        }
    }
    @keyframes fade_in {
        0% {
            opacity: 0%;
        }
        50% {
            opacity: 0%;
        }
        100% {
            opacity: 100%;
        }
    }

    @media screen and (min-width:992px) {
        .ladning_background {
            width: 100%;
            height: auto;
        }
        .center {
            width: 60%;
            h1 {
                font-size: 50px;
            }
            p {
                font-size: 28px;
            }
        }
        .scroll {
            width: 100%;
            bottom: 5%;
            h1 {
                font-size: 40px;
            }
        }
    }

    @media screen and (min-width:1440px) {
        .center {
            width: 40%;
        }
    }
</style>