<template>
  <div class="footer">
      <ul class="contatti">
          <li>Contatti</li>
          <li><a href="mailto:castellazzivalentina0@gmail.com"><i class="far fa-envelope"> email</i></a></li>
          <li>Indirizzo ufficio</li>
          <li>Numero di telefono</li>
      </ul>
      <ul class="inline_menu">
        <li>
          <a href="https://www.instagram.com/cv_weddingsandevents/" target="_blank"><i class="fab fa-instagram"></i></a>
        </li>
        <li>
          <a href="https://www.tiktok.com/@cv_weddingsandevents" target="_blank"><i class="fab fa-tiktok"></i></a>
        </li>
        <li>
          <a href="" target="_blank"><i class="fab fa-twitter"></i></a>
        </li>
        <li>
          <a href="" target="_blank"><i class="fab fa-linkedin-in"></i></a>
        </li>
      </ul>
      <p class="copy">&copy; Copyright protected</p>
  </div>
</template>

<script>
export default {
    name:'Footer',
    props: {
        linguaggio: String
    }
}
</script>

<style lang="scss" scoped>
.footer {
    position: relative;
    height: 40vh;
    background-color: gold;
}
.contatti {
    padding-top: 20px;
    list-style: none;
    margin-left: 20px;
    color: white;
    li:first-child {
        font-size: 20px;
        font-weight: 800;
    }
}
.inline_menu {
    list-style: none;
    margin-left: 20px;
    margin-top: 20px;
    li {
        display: inline-block;
        margin: 5px;
        a {
            color: white;
            &:hover {
                color: #feb5af;
            }
        }
    }
}

.copy {
    font-size: 8px;
    color: white;
    position: absolute;
    bottom: 5px;
    left: 50%;
    transform: translateX(-50%);
}
</style>