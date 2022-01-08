!<template>
  <!-- Qui ci sarà la descrizione dell'azienda -->
  <div class="brand_DescContainer clearfix">
    <!-- Questo è il logo dell'azienda -->
    <img src="../assets/logo.png" alt="Logo azienda" class="logo_azienda">
    
    <p class="text">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quod at minus fugiat asperiores error velit nisi nesciunt quae, reiciendis repudiandae incidunt. Ipsum iusto obcaecati maxime deleniti odit nostrum soluta consectetur molestiae nam voluptatum, saepe incidunt ipsa similique quis sint ad consequuntur! Unde ab minima saepe cupiditate blanditiis eaque eum facere porro, minus incidunt sed, ullam labore eos officia, commodi consequatur maiores obcaecati ipsa nostrum. Reiciendis quidem veritatis culpa aliquam deleniti!</p>
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
  margin-top: 20px;
  padding-left: 10px;
  padding-right: 10px;
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
.clearfix {
    content: "";
    display: table;
    clear: both;
}

</style>