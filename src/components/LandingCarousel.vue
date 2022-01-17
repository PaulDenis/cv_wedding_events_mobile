!<template>
<div class="wrapper">
    <div class="title">
        <h1 v-if="linguaggio == 'italiano'">Le ultime aggiunte</h1>
        <h1 v-if="linguaggio == 'inglese'">Latest pictures</h1>
    </div>

    <!-- L'immagine cambia ogni 6 secondi -->
    <!-- Aggiungere in futuro un collegamento al server dove si troveranno le foto -->
    <div class="carusel">
        <div v-on:click="goback()">
            <i class="fas fa-chevron-circle-left navigation"></i>
        </div>
        <div class="carusel_container">
            <!-- <img :src="immagini[prev()].link" alt="Tavolo con fiori" class="secondary_image image_left"> -->
            <img :src="immagini[(current_picture)].link" alt="Tavolo con fiori" id="primary_image">
            <!-- <img :src="immagini[next()].link" alt="Tavolo con fiori" class="secondary_image image_right"> -->
        </div>
        <div v-on:click="goForward()">
            <i class="fas fa-chevron-circle-right navigation"></i>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'LandingCarousel',
    props: {
        linguaggio: String
    },
    data() {
        return {
            immagini: [
                {
                link: require('../assets/flower_table.jpg'),
                id: 0
                },
                { 
                link: require('../assets/round_flower_table.jpeg'),
                id: 1
                },
                {
                link: require('../assets/evening_table.jpg'),
                id: 2
                }],
            current_picture: 0,
            clock: null
        }
    },
    methods: {
       goForward: function() {
            this.current_picture++;
            if(this.current_picture == this.immagini.length) {
                this.current_picture = 0;
            }
        },
        goback: function() {
            this.current_picture--;
            if(this.current_picture < 0) {
                this.current_picture = this.immagini.length-1;
            }
        },
        prev: function() {
            var prev = this.current_picture - 1;
            if (this.current_picture == 0) {
                return prev = this.immagini.length-1;
            }
            return prev;
        },
        next: function() {
            var next = this.current_picture + 1;
            if (this.current_picture == (this.immagini.length-1)) {
                return next = 0;
            }
            return next;
        }
    },
    mounted() {
        this.clock = setInterval(() => {
                this.goForward();
            }, 6000);
    },
    beforeUpdate () {
        clearInterval(this.clock);
    },
    updated () {
        this.clock = setInterval(() => {
            this.goForward();
        }, 6000);
    }
    
}
</script>

<style lang="scss" scoped>
    .wrapper {
        background-color: #eb98a8;
        text-align: center;
    }
    .carusel {
        display: flex;
        align-items: center;
        justify-content: space-around;
        height: 30vh;
        .carusel_container {
            align-self: center;
            height: 90%;
            img {
                position: relative;
                height: 100%;
            }
        }
    }
    .title {
        color: #bc8d34;
        text-shadow: 1px 1px 2px black;
        h1 {
            font-family: 'Sacramento';
            font-size: 50px;
        }
    }
    #primary_image {
        z-index: 3;
    }
    .navigation {
        margin-left: 10px;
        margin-right: 10px;
        font-size: 20px;
    }

    @media  screen and (min-width: 992px) {
        .wrapper {
            padding-top: 20px;
            padding-bottom: 30px;
            height: auto;
        }
        .carusel {
            height: 60vh;
            .carusel_container {
                img {
                    top: 0;
                    width: auto;
                    height: 100%;
                }
            }
        }
        .navigation {
            font-size: 40px;
        }
    }


</style>