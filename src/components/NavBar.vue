!<template>
    <nav>
        <div class="nav_btn" v-on:click="show=true" v-if="show==false">
            <i class="fas fa-bars"></i>
        </div>
        <div class="navigation_menu" v-if="show" :class="deleting ? 'deleting' : ''">
            <!-- Al click sull'immagine si torna alla home -->
            <img src="../assets/logo.png" alt="" v-on:click="current_page='home', $emit('pagina', current_page)">
            <i class="fas fa-times" v-on:click="outAnim()"></i>

            <!-- menu inglese -->
            <ul v-if="linguaggio=='inglese'">
                <li 
                v-on:click="current_page='home', $emit('pagina', current_page)"
                :class="pagina_corrente=='home' ? 'current' : ''">Home Page</li>
                <li 
                v-on:click="current_page='type of events', $emit('pagina', current_page)"
                :class="pagina_corrente=='type of events' ? 'current' : ''">Type of events</li>
                <li 
                v-on:click="current_page='innovative ideas', $emit('pagina', current_page)"
                :class="pagina_corrente=='innovative ideas' ? 'current' : ''">Innovative ideas</li>
                <li 
                v-on:click="current_page='galleria', $emit('pagina', current_page)"
                :class="pagina_corrente=='galleria' ? 'current' : ''">Gallery</li>
                <li 
                v-on:click="current_page='about us', $emit('pagina', current_page)"
                :class="pagina_corrente=='about us' ? 'current' : ''">About us</li>
                <li 
                v-on:click="current_page='contatti', $emit('pagina', current_page)"
                :class="pagina_corrente=='contatti' ? 'current' : ''">Contacts</li>
            </ul>
            
            <!-- menu italiano -->
            <ul v-if="linguaggio=='italiano'">
                <li 
                v-on:click="current_page='home', $emit('pagina', current_page)"
                :class="pagina_corrente=='home' ? 'current' : ''">Home</li>
                                <li 
                v-on:click="current_page='type of events', $emit('pagina', current_page)"
                :class="pagina_corrente=='type of events' ? 'current' : ''">Tipi di eventi</li>
                <li 
                v-on:click="current_page='innovative ideas', $emit('pagina', current_page)"
                :class="pagina_corrente=='innovative ideas' ? 'current' : ''">Idee innovative</li>
                <li 
                v-on:click="current_page='galleria', $emit('pagina', current_page)"
                :class="pagina_corrente=='galleria' ? 'current' : ''">Galleria</li>
                <li 
                v-on:click="current_page='about us', $emit('pagina', current_page)"
                :class="pagina_corrente=='about us' ? 'current' : ''">Su di noi</li>
                <li 
                v-on:click="current_page='contatti', $emit('pagina', current_page)"
                :class="pagina_corrente=='contatti' ? 'current' : ''">Contatti</li>
            </ul>
        </div>
    </nav>
</template>

<script>

export default {
    name:'NavBar',
    props: {
        linguaggio: String,
        pagina_corrente: String
    },
    data() {
        return {
            show: false,
            deleting:false,
            current_page: 'home'
        }
    },
    methods: {
        outAnim: function() {
            this.deleting=true;
            this.clock = setTimeout(() => {
                this.show=false;
                this.deleting=false;
            }, 1000);
        } 
    }
}
</script>

<style lang="scss" scoped>
nav {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 10;
}
.nav_btn {
    padding: 10px;
    i:hover {
        cursor: pointer;
    }
    &:focus {
        background-color: white;
    }
}
.navigation_menu {
    width: 200px;
    background-color: white;
    border: 1px solid black;
    ul {
        list-style: none;
        padding: 0;
        margin: 0;
        li {
            padding: 2px 10px 5px 10px;
            &:nth-child(2n-1) {
                background-color: #ffb5af;
            }
            &:hover {
                cursor: pointer;
            }
        }
    }
    img {
        height: 30px;
        border-radius: 50%;
        margin: 5px;
        margin-left: 10px;
        margin-bottom: 15px;
        &:hover {
            cursor: pointer;
        }
    }
    animation: slide_in 1s;
}
.fa-times {
    position: relative;
    left: 130px;
    bottom: 3px;
    &:hover {
        cursor: pointer;
    }
}
.deleting {
    animation: slide_out 1s;
}
.current {
    border-left: 5px solid #bc8d34;
}

@keyframes slide_in {
    0% {
        position: relative;
        right: 200px;
    }
    100% {
        position: relative;
        right: 0;
    } 
}
@keyframes slide_out {
    0% {
        position: relative;
        right: 0;
    } 
    100% {
        position: relative;
        right: 200px;
    }
}

</style>