<template>
  <div class="containerLogos">
    <div class="cardLogo">
      <img src="../assets/img/lorem-1.png" />
    </div>
    <div class="cardLogo">
      <img src="../assets/img/lorem-2.png" />
    </div>
    <div class="cardLogo">
      <img src="../assets/img/lorem-3.png" />
    </div>
    <div class="cardLogo">
      <img src="../assets/img/Logo.png" />
    </div>
    <div class="cardLogo">
      <img src="../assets/img/lorem-4.png" />
    </div>
    <div class="cardLogo">
      <img src="../assets/img/lorem-5.png" />
    </div>
  </div>
</template>
<script>
export default{
  name: "Logos"
}
</script>
<style scoped>
.containerLogos{
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 50px;
}

@media screen and (max-width: 769px){
  .containerLogos{
    display: grid !important;
    grid-template-columns: repeat(3, 1fr);
    justify-content: center;
    place-items: center;
  }
}
@media screen and (max-width: 376px){
  .containerLogos{
    margin-top: 80px;
    gap: 5px;
  }
  .containerLogos img{
    width: 100px;
  }
}
</style>
