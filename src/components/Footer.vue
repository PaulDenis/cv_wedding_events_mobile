<template>
  <div class="footer">
      <ul class="contatti">
        <!-- Tutti i contatti di Valentina -->
          <li v-if="linguaggio=='italiano'">Contatti</li>
          <li v-if="linguaggio=='inglese'">Contacts</li>
          <li><a href="mailto:castellazzivalentina0@gmail.com" target="_blank"><i class="far fa-envelope"> castellazzivalentina0@gmail.com</i></a></li>
          <li>Via Roma n°1, Modena (MO)</li>
          <li>+39 123 123 1234</li>
          <li>
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
          </li>
      </ul>
      <div class="creator">
        <!-- La mia pagina instagram -->
        <p v-if="linguaggio=='inglese'">Created by <a href="https://www.instagram.com/goddenix/" target="_blank" rel="noopener noreferrer">Paul Denis</a></p>
        <p v-if="linguaggio=='italiano'">Creato da <a href="https://www.instagram.com/goddenix/" target="_blank" rel="noopener noreferrer">Paul Denis</a></p>
        <img src="../assets/DenixLogo.png" alt="Creator Logo">
      </div>
      <!-- copyright -->
      <p class="copy" v-if="linguaggio=='inglese'">&copy; Copyright protected</p>
      <p class="copy" v-if="linguaggio=='italiano'">&copy; Protetto da copyright</p>
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
    height: 30vh;
    background-color: #bc8d34;
}
.contatti {
    float: left;
    padding: 0;
    padding-top: 5px;
    list-style: none;
    color: white;
    li:first-child {
        font-size: 20px;
        font-weight: 800;
    }
    li {
      margin: 10px;
      a {
        color: white;
      }
    }
}
.inline_menu {
    list-style: none;
    padding: 0;
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
.creator {
  position: absolute;
  display: flex;
  align-items: center;
  bottom: 15px;
  right: 10px;
  text-align: right;
  color: white;
  img {
    display: inline-block;
    height: 25px;
  }
  p {
    font-size: 12px;
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