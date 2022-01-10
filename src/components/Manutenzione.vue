!<template>
<div class="manutenzione_container">
    <div v-show="linguaggio == 'italiano'" class="center">
        <h1>Questa pagina è in manutenzione</h1>
    </div>

      <!-- Versione inglese -->
    <div v-show="linguaggio == 'inglese'" class="center">
        <h1>This page is under maintenance</h1>
    </div>


</div>
</template>

<script>
export default {
    name: 'Manutenzione',
    props: {
        linguaggio: String
    }
}
</script>

<style lang="scss" scoped>
    .manutenzione_container {
        width: 100%;
        height: 100vh;
        background-color: #ffb5af;
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
        background-color: rgba(256, 256, 256, 1);
        h1 {
            font-size: 30px;
            .gold {
                color: #bc8d34;
            } 

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
</style>