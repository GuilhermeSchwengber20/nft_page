<template>
  <div class="containerOwner">
    <div class="title">
      <h2>Our Team</h2>
      <p>
        Risus commodo id odio turpis pharetra elementum. Pulvinar porta porta feugiat scelerisque in elit. Morbi rhoncus, tellus, eros consequat magna semper orci a tincidunt.
      </p>
    </div>
    <div class="containerBox">
      <div class="box" v-for="card in cards" :key="card.name">
        <div class="boxImg">
          <img :src="card.icon" />
        </div>
        <div class="boxText">
          <h4>{{ card.nome }}</h4>
          <p>{{ card.cargo }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: "OwnerSection",
  data(){
    return {
      cards: [
        {
          icon: require("../assets/img/team-1.png"),
          nome: "Guy Hawkins",
          cargo: "CEO",
        },
        {
          icon: require("../assets/img/team-2.png"),
          nome: "Jane Cooper",
          cargo: "COO",
        },
        {
          icon: require("../assets/img/team-3.png"),
          nome: "Darrell Steward",
          cargo: "CTO",
        },
        {
          icon: require("../assets/img/team-4.png"),
          nome: "Dianne Russell",
          cargo: "CDO",
        },
      ]
    }
  }
}
</script>
<style scoped>
.containerOwner{
  width: 100%;
  height: 60vh;
  padding: 40px 0px;
  display: flex;
  flex-direction: column;
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
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  padding: 70px 0px;
}

.box{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.box .boxText{
  text-align: center;
}

.box .boxText h4{
  font-weight: 700;
  font-family: var(--fontPadrao);
  font-size: 24px;
}

.box .boxText p{
  font-family: var(--fontPadrao);
  font-size: 14px;
  margin-top: 10px;
}

@media screen and (max-width: 769px){

  .title p{
    font-family: var(--fontPadrao);
    width: 680px;
  }
}

@media screen and (max-width: 376px){
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
    width: 100%;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
  }
  .box{
    flex-wrap: wrap;
    white-space: wrap;
  }
}
</style>
