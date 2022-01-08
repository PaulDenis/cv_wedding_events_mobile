<template>
  <div class="footer">
      <ul class="contatti">
          <li>Contatti</li>
          <li><a href="mailto:castellazzivalentina0@gmail.com"><i class="far fa-envelope"> castellazzivalentina0@gmail.com</i></a></li>
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
        <img src="../assets/DenixLogo.png" alt="Creator Logo">
        <p>Created by <a href="http://" target="_blank" rel="noopener noreferrer">Paul Denis</a></p>
      </div>
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
    height: 20vh;
    background-color: gold;
}
.contatti {
    float: left;
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