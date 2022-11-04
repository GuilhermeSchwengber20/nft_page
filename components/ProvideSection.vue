<template>
  <div class="containerProvide">
    <div class="title">
      <h2>We Provide</h2>
      <p>
        Risus commodo id odio turpis pharetra elementum. Pulvinar porta porta feugiat scelerisque in elit. Morbi rhoncus, tellus, eros consequat magna semper orci a tincidunt.
      </p>
    </div>
    <div class="containerBox">
      <div class="box" v-for="card in cards" :key="card.title">
        <div class="boxIcon">
          <img :src="card.icon" />
        </div>
        <div class="boxTitle">
          <h3>{{ card.title }}</h3>
        </div>
        <div class="boxText">
          <p>{{ card.text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: "ProvideSection",
  data(){
    return{
      cards: [
        {
          icon: require("../assets/img/icone-1.png"),
          title: "Host your NFTs",
          text: "Egestas tellus nunc proin amet tellus tincidunt lacus consequat. Ultrices",
        },
        {
          icon: require("../assets/img/icone-2.png"),
          title: "See your sales",
          text: "Integer ante non nunc, eget est justo vel semper nunc. Lacus ",
        },
        {
          icon: require("../assets/img/icone-3.png"),
          title: "Secure wallet",
          text: "Sed faucibus faucibus egestas volutpat, accumsan adipiscing egestas est. Auctor et leo urna est. ",
        },
        {
          icon: require("../assets/img/icone-4.png"),
          title: "No scam",
          text: "Sed faucibus faucibus egestas volutpat, accumsan adipiscing egestas est. Auctor et leo urna est.",
        },
      ]
    }
  }
}
</script>
<style scoped>
.containerProvide{
  width: 100%;
  padding: 60px 0px;
}

.title{
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
.title h2{
  font-family: var(--fontTitle);
  font-weight: 700;
  font-size: 40px;
  font-style: normal;
  height: 65px;
}

.title p{
  font-family: var(--fontPadrao);
  width: 860px;
}

.containerBox{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  padding: 30px 0px;
  align-items: start;
  margin-top: 30px;
}

.box{
  display: flex;
  flex-direction: column;
  width: 200px;
  align-items: center;
  text-align: center;
}
.box .boxTitle{
  font-family: var(--fontPadrao);
  font-size: 18px;
  font-weight: 700;
}

.box .boxText{
  font-family: var(--fontPadrao);
  font-size: 14px;
  margin-top: 10px;
}


@media screen and (max-width: 769px){
  .title p{
    font-family: var(--fontPadrao);
    width: 580px;
  }
  .containerBox{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    place-items: center;
    justify-content: center;
  }
  .box{
    margin-bottom: 10px;
  }
  .boxText{
    width: 340px;
  }
}
@media screen and (max-width: 376px){
  .containerProvide{
    padding: 0;
    margin-top: 290px;
  }
  .title p{
    font-family: var(--fontPadrao);
    width: 320px;
  }
  .title h2{
    font-family: var(--fontTitle);
    font-weight: 700;
    font-size: 30px;
    font-style: normal;
    height: 65px;
  }
  .containerBox{
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    place-items: center;
    justify-content: center;
  }
  .boxText{
    width: 300px;
  }
}
</style>
