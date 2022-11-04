<template>
  <div class="containerNft">
    <div class="title">
      <h2>Hottest Collections</h2>
      <p>Risus commodo id odio turpis pharetra elementum. Pulvinar porta porta feugiat scelerisque in elit. Morbi rhoncus, tellus, eros consequat magna semper orci a tincidunt. </p>
    </div>
    <div class="containerCard">
      <div class="box" v-for="card in cards" :key="card.id">
        <div class="imgBox">
          <img :src="card.image" />
        </div>
        <div class="titleBox">
          <h3>{{ card.title }}</h3>
        </div>
        <div class="textBox">
          <p>{{ card.text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: "NFTSection",
  data(){
    return {
      cards: [
        {
          id: 1,
          image: require("../assets/img/nft-1.png"),
          title: "Moonbirds",
          text: "Faucibus odio elementum nulla venenatis, libero. Ullamcorper duis fringilla pulvinar nibh diam sit."
        },
        {
          id: 2,
          image: require("../assets/img/nft-2.png"),
          title: "Clone X - X Takashi Murakami",
          text: "Magna in condimentum praesent pretium vitae mattis facilisis nunc. Lectus in ac ac."
        },
        {
          id: 3,
          image: require("../assets/img/nft-3.png"),
          title: "Mutant Ape Yatch Club",
          text: "Sit aenean porttitor sit lectus. Adipiscing egestas etiam eget cursus nulla risus euismod. Netus."
        },
        {
          id: 4,
          image: require("../assets/img/nft-4.png"),
          title: "'MOAR' by Joan Cornella",
          text: "Faucibus odio elementum nulla venenatis, libero. Ullamcorper duis fringilla pulvinar nibh diam sit."
        },
        {
          id: 5,
          image: require("../assets/img/nft-5.png"),
          title: "Doodles",
          text: "Magna in condimentum praesent pretium vitae mattis facilisis nunc. Lectus in ac ac."
        },
        {
          id: 6,
          image: require("../assets/img/nft-6.png"),
          title: "KIWAMI Genesis",
          text: "Sit aenean porttitor sit lectus. Adipiscing egestas etiam eget cursus nulla risus euismod. Netus."
        },
        {
          id: 7,
          image: require("../assets/img/nft-7.png"),
          title: "Arcane Land",
          text: "Faucibus odio elementum nulla venenatis, libero. Ullamcorper duis fringilla pulvinar nibh diam sit."
        },
        {
          id: 8,
          image: require("../assets/img/nft-8.png"),
          title: "Goons of Balatroon",
          text: "Magna in condimentum praesent pretium vitae mattis facilisis nunc. Lectus in ac ac."
        },
        {
          id: 9,
          image: require("../assets/img/nft-9.png"),
          title: "Meta Toy DragonZ",
          text: "Sit aenean porttitor sit lectus. Adipiscing egestas etiam eget cursus nulla risus euismod. Netus."
        },
      ]
    }
  }
}
</script>
<style scoped>
.containerNft{
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 80px 0px;
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
.containerCard{
  width: 100%;
  display: grid;
  grid-template-columns: repeat(3, 0.3fr);
  justify-content: center;
  justify-items: center;
  align-items: start;
}

.box{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 350px;
  height: auto;
  margin-top: 50px;
}
.imgBox img{
  width: 350px;
  height: 100%;
}

.box .titleBox h3{
  font-family: var(--fontTitle);
  text-align: center;
  line-height: 30px;
  font-size: 25px;
  margin-top: 10px;
}
.box .textBox p{
  font-family: var(--fontPadrao);
  margin-top: 6px;
  text-align: center;
  width: 100%;
  font-size: 14px;
}

@media screen and (max-width: 769px){
  .box img{
    width: 250px;
    height: 400px;
    object-fit: cover;
    border-radius: 20px;
  }
  .containerCard{
    column-gap: 10px;
  }
  .box{
    width: 250px;
  }

  .title p{
    font-family: var(--fontPadrao);
    width: 660px;
  }
}
@media screen and (max-width: 376px){
  .title h2{
    font-size: 26px;
  }
  .title p{
    font-family: var(--fontPadrao);
    width: 320px;
  }
  .containerCard{
    width: 100%;
    display: grid;
    grid-template-columns: repeat(1, 0.3fr);
    justify-content: center;
    justify-items: center;
    align-items: start;
  }
  .box img{
    width: 300px;
    height: 400px;
    object-fit: cover;
    border-radius: 20px;
  }
  .box{
    width: 320px;
  }
}
</style>
