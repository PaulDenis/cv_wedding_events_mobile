!<template>
  <div class="personal_Desc">
      <img src="../assets/Vale.jpeg" alt="Valentina CEO" class="personal_img">
      <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Illum saepe commodi ducimus consequuntur. Temporibus vero, aliquid sed aspernatur eligendi dolor animi voluptas obcaecati, ipsum, cum accusantium quidem adipisci nostrum laboriosam unde nemo veritatis quas nisi? Vero eum blanditiis cum ut recusandae aut reiciendis dicta illum rerum necessitatibus, molestias, ducimus incidunt!</p>
  </div>
</template>

<script>
export default {
    name: 'PersonalDesc',
    props: {
        linguaggio: String
    }
}
</script>

<style lang="scss" scoped>
    .personal_Desc {
        padding: 5px;
        margin-bottom: 10px;
        text-align: right;
        text-align: justify;
        p {
            padding: 5px;
        }
        &::after {
            content:"";
            display: table;
            clear: both;
        }
    }
    .personal_img {
        float: right;
        height: 150px;
        border-radius: 50%;
        margin-left: 30px;
        shape-outside: circle();
    }

    @media screen and (min-width: 992px) {
        .personal_Desc {
            display: flex;
            flex-direction: row-reverse;
            align-items: center;
        }
    }


</style>