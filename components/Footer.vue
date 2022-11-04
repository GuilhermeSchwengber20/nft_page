<template>
  <div class="containerFooter">
    <div class="containerContent">
      <div class="menu">
        <a>Terms & Conditions</a>
        <a>Privacy Policy</a>
      </div>
      <div class="logo">
        <img src="../assets/img/Logo.png" />
      </div>
      <div class="menu">
        <a>Cookies</a>
        <a>Refounds</a>
        <a>License</a>
      </div>
    </div>
    <hr />
    <div class="copyright">
      <p>Desenvolvido por <a>Guilherme Schwengber</a></p>
    </div>
  </div>
</template>
<script>
export default{
  name: "Footer"
}
</script>
<style scoped>
.containerFooter{
  margin-top: 140px;
  width: 100%;
}

.containerContent{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  padding-bottom: 10px;
}
.menu a {
  font-family: var(--fontPadrao);
  font-weight: 300;
  margin-right: 30px;
}
.copyright{
  text-align: center;
  font-family: var(--fontPadrao);
}

@media screen and (max-width: 769px){
  .menu a{
    margin-right: 10px;
  }
}
.logo{
  display: flex;
}
@media screen and (max-width: 376px){

  .menu .logo{
    display: none !important;
  }
}
</style>
