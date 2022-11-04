<template>
  <div class="containerNewsletter">
    <div class="containerBackground">
      <div class="containerContent">
        <h2>Ready to sell your NFTs?</h2>
        <p>Risus commodo id odio turpis pharetra elementum. Pulvinar porta porta feugiat scelerisque in elit. Morbi rhoncus, tellus, eros consequat magna semper orci a tincidunt. </p>
        <button>
          Sell right now
        </button>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: "Newsletter"
}
</script>
<style scoped>
.containerNewsletter{
  width: 100%;
  height: 100%;
  margin: auto;
}
.containerBackground{
  margin: auto;
  width: 90%;
  height: 50vh;
  border: 1px solid #D6BCFA;
  background: #FCFAFF;
  box-shadow: inset 0px 0px 50px #F8E0FA;
  border-radius: 60px;
  padding: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.containerContent{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.containerContent h2{
  font-family: var(--fontTitle);
  font-weight: 700;
  font-size: 38px;
}

.containerContent p{
  font-family: var(--fontPadrao);
  font-weight: 300;
  font-size: 14px;
  width: 680px;
  margin-top: 10px;
  text-align: center;
}
button{
  margin-top: 20px;
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
  .containerContent h2{
    font-family: var(--fontTitle);
    font-weight: 700;
    font-size: 20px;
  }
  .containerContent p{
    font-family: var(--fontPadrao);
    font-weight: 300;
    font-size: 14px;
    width: 300px;
    margin-top: 10px;
    text-align: center;
  }
}
</style>
