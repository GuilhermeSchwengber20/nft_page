<template>
  <div class="containerHome">
    <div class="containerTitle">
      <h2> Create & sell your NFTs today</h2>
    </div>
    <div class="containerText">
      <p>
        Velit, odio bibendum eu, viverra sit laoreet posuere. Ut scelerisque posuere massa amet. Ornare lacinia vitae at vestibulum morbi.
        Volutpat libero curabitur feugiat risus dui pulvinar. Elementum.
      </p>
    </div>
    <div class="containerButton">
      <button>Let's sell</button>
    </div>
  </div>
</template>
<script>
export default{
  name:"Home"
}
</script>
<style scoped>
.containerHome{
  width: 100%;
  height: 81vh;
  padding: 80px 0px;
  background-image: url("../assets/img/Background.png");
  background-position: center;
}

.containerTitle{
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin: auto;
  width: 650px;
  height: 200px;

}
.containerTitle h2{
  text-align: center;
  font-family: var(--fontTitle);
  text-shadow: 5px 5px 0px #FFFFFF;
  font-size: 70px;
  font-weight: 700;
  font-style: normal;
}

.containerText{
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin: auto;
  width: 770px;
}
.containerText p{
  font-family: var(--fontPadrao);
  font-weight: 400;
  text-align: center;
  line-height: 24px;
}
.containerButton{
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin-top: 25px;
}
.containerButton button{
  display: flex;
  font-family: var(--fontTitle);
  color: #ffff;
  font-weight: 700;
  border: none;
  padding: 15px;
  height: 40px;
  letter-spacing: 1px;
  border-radius: 9px;
  background: var(--btnColor);
  align-items: center;

}

@media screen and (max-width: 376px){
  .containerTitle h2{
    font-size: 42px;
  }
  .containerTitle{
    width: 350px;
  }
  .containerText{
    width: 300px;
  }
}

</style>
