!<template>
  <div class="personal_Desc">
      <img src="../assets/Vale.jpeg" alt="Valentina CEO" class="personal_img">
      <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Illum saepe commodi ducimus consequuntur. Temporibus vero, aliquid sed aspernatur eligendi dolor animi voluptas obcaecati, ipsum, cum accusantium quidem adipisci nostrum laboriosam unde nemo veritatis quas nisi? Vero eum blanditiis cum ut recusandae aut reiciendis dicta illum rerum necessitatibus, molestias, ducimus incidunt!</p>
  </div>
</template>

<script>
export default {
    name: 'PersonalDesc'
}
</script>

<style lang="scss" scoped>
.personal_Desc {
    p {
        padding: 5px;
    }
}
.personal_img {
    float: right;
    height: 150px;
    border-radius: 50%;
    margin-left: 50px;
    shape-outside: ellipse(60% 60% at 90%);
}

</style>