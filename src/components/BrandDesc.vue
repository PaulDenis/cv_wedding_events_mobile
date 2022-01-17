!<template>
  <!-- Qui si trova la descrizione dell'azienda -->
  <div class="brand_DescContainer clearfix" id="brand">
    <!-- Questo è il logo dell'azienda -->
    <img src="../assets/logo.png" alt="Logo azienda" class="logo_azienda">
    <h1>You are your only limit</h1>
    <p class="text" v-if="linguaggio == 'italiano'">'You are your only limit', che si traduce in "Tu sei il tuo unico limite". 
      <br>
      Questa frase è stata, ed è tutt'ora, il principio su cui si basa la mia vita. Essa racchiude l'essenza della perseveranza, del non arrendersi di fronte agli ostacoli e sopratutto di esprimere quello in cui credo da sempre: nessuno può dirti cosa puoi o non puoi fare, se ci credi davvero raggiungerai i tuoi obbiettivi.
      <br>
      Può sembrare una frase fatta, e in effetti un pò lo è, ma è basata su un concetto della psicologia che si chiama "profezia che si autoavvera". Questa profezia consiste in una previsione, che si realizza per il solo fatto di essere stata espressa. Perchè? Perchè quando crediamo fermamente in qualcosa agiamo per fare in modo che accada. Per questo la ripropongo a voi, perchè è proprio ciò su cui si basa la mia missione: realizzare i vostri desideri, al massimo delle possibilità, per rendere il vostro giorno unico ed indimenticabile... Dopotutto è uno dei giorni più importanti della vostra vita!
      <br>
      Fare in modo che i vostri sogni si avverino e vedere i vostri volti pieni di gioia è la soddisfazione più grande a cui possa ambire. Dopotutto alle favole ci crediamo un pò tutti... Perchè non trasformarle in realtà?
    </p>
    <p class="text" v-if="linguaggio == 'inglese'">
      This phrase was, and still is, the principle on which my life is based. It contains the essence of perseverance, of never giving up in front of obstacles and, more important, to always express what you believe in: no one can tell you what you can or can not do, if you really believe in it, you will achieve your goals.
      <br>
      It may sound like a clichè, and it is a bit, but it's based on a concept of psychology named "self-fulfilling prophecy". This provecy consist in a forecast that realize itself for the only fact that it was expressed. Why? Because when we really believe in something we act to make it happen. That's why I propose it to you too, because on my mission is based on this: realizing your dreams, at the maximum of possibilyties, to make your day unic and unforgettable... After all is one of the most important days in your life!
      <br>
      To make sure that your dreams come true and see your faces full of joy is the biggest accomplishment I can dream of. Deep inside everyone believe in fairy tales... Why not turn them into reality?
    </p>
  </div>
</template>

<script>
export default {
    name: 'BrandDesc',
    props: {
        linguaggio: String
    }
}
</script>

<style lang="scss" scoped>
.brand_DescContainer {
  height: 25vh;
  width: 100%;
  margin-top: 20px;
  padding-left: 10px;
  padding-right: 10px;
  h1 {
    color: #bc8d34;
  }
}
.text {
  text-align: justify;
  font-size: 15px;
}
.logo_azienda {
  margin-right: 30px;
  margin-top: 20px;
  height: 150px;
  float: left;
  shape-outside: circle(50%);
  border-radius: 50%;
}
.clearfix {
    content: "";
    display: table;
    clear: both;
}

</style>