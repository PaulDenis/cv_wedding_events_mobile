!<template>
  <!-- Qui ci sarà la descrizione dell'azienda -->
  <div class="brand_DescContainer">
    <!-- Questo è il logo dell'azienda -->
    <img src="../assets/logo.png" alt="Logo azienda" class="logo_azienda">
    
    <p class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nobis error sapiente, alias rem quasi eveniet odio voluptates accusamus in quas vitae quo reprehenderit doloremque earum commodi, blanditiis ea aliquid soluta fugiat corporis atque dolor voluptate accusantium. Molestiae dolor nisi maiores! Tempora praesentium aut molestias rerum nemo. Ex repellendus cumque delectus labore officia? Sed beatae aut dignissimos enim assumenda quam qui voluptas accusantium rem sint fugiat magni deleniti saepe minus commodi consequuntur eius vitae consectetur suscipit, atque exercitationem, aspernatur architecto quis? Non, nesciunt at dignissimos consequatur officia odio rem animi totam cumque esse inventore nemo quidem numquam iure, dolores reprehenderit eaque?</p>
  </div>
</template>

<script>
export default {
    name: 'BrandDesc'
}
</script>

<style lang="scss" scoped>
.brand_DescContainer {
  height: 30vh;
}
.text {
  text-align: justify;
  font-size: 16px;
}
.logo_azienda {
  margin-right: 50px;
  height: 150px;
  float: left;
  shape-outside: circle();
  border-radius: 50%;
}

</style>