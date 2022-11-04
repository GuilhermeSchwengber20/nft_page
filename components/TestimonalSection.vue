<template>
  <div class="containerTestimonal">
    <div class="title">
      <h2>Testimonials</h2>
    </div>
    <div class="containerGrid">
      <div class="card" v-for="card in cards" :key="card.nome" :id="card.id">
        <div class="headerCard">
          <div>
            <img :src="card.icon" />
          </div>
          <div>
            <span>{{card.nome }}</span>
            <p>{{ card.insta }}</p>
          </div>
        </div>
        <div class="bodyCard">
          <p>{{ card.text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: "TestimonalSection",
  data (){
    return {
      cards: [
        {
          id: "brooklynsimmons",
          icon: require("../assets/img/avatar-1.png"),
          nome: "Brooklyn Simmons",
          insta: "@brooklynsimmons",
          text: "Sit ut diam bibendum dolor. Ullamcorper pharetra nibh eget vitae pulvinar. Placerat sapien, dolor, aenean vivamus in tincidunt et. Mauris dolor vestibulum et lacus a ante orci."
        },
        {
          id: "estherhoward",
          icon: require("../assets/img/avatar-2.png"),
          nome: "Esther Howard",
          insta: "@estherhoward",
          text: "Vitae tellus bibendum nibh integer auctor pretium sed. Sollicitudin tristique euismod elit."
        },
        {
          id: "kristinwatson",
          icon: require("../assets/img/avatar-3.png"),
          nome: "Kristin Watson",
          insta: "@kristinwatson",
          text: "Lectus dolor fermentum gravida ut sit vel. Enim. Lorem ipsum will never be the same again so purchase Zeus UI now or web trying."
        },
        {
          id: "DianneRussell",
          icon: require("../assets/img/avatar-4.png"),
          nome: "Dianne Russell",
          insta: "@DianneRussell",
          text: "Eu luctus tincidunt vulputate praesent interdum proin. Magna gravida at pretium vitae. Viverra."
        },
        {
          id: "ArieneMcCoy",
          icon: require("../assets/img/avatar-5.png"),
          nome: "Ariene McCoy",
          insta: "@ArieneMcCoy",
          text: "Sit ut diam bibendum dolor. Ullamcorper pharetra nibh eget vitae pulvinar. Placerat sapien, dolor, aenean vivamus in tincidunt et. Mauris dolor vestibulum et lacus a ante orci."
        },
        {
          id: "LeslieAlexander",
          icon: require("../assets/img/avatar-6.png"),
          nome: "Leslie Alexander",
          insta: "@LeslieAlexander",
          text: "Varius bibendum quis ipsum sit. Enim ante donec erat neque semper. Consectetur sed imperdiet tortor duis nulla aliquet at integer. "
        },
        {
          id: "EleanorPena",
          icon: require("../assets/img/avatar-7.png"),
          nome: "Eleanor Pena",
          insta: "@EleanorPena",
          text: "Amet quam velit nisl et et. Fusce ante facilisi vulputate eget aliquet mi sem eu vulputate."
        },
        {
          id: "JaneCooper",
          icon: require("../assets/img/avatar-8.png"),
          nome: "Jane Cooper",
          insta: "@JaneCooper",
          text: "Amet aliquam, volutpat nisl, duis sed at. Vehicula proin consectetur risus dictumst nec amet consequat at tempus. Ornare dapibus nunc fames nibh morbi viverra eu sed mattis. "
        },
        {
          id: "DarleneRobertson",
          icon: require("../assets/img/avatar-1.png"),
          nome: "Darlene Robertson",
          insta: "@DarleneRobertson",
          text: "Imperdiet sed tellus tempor vitae elit a. Arcu a."
        },

      ]
    }
  },
  mounted(){
    window.addEventListener("scroll", (e) => {
      const container = document.querySelector(".containerGrid");
      let value = 0
      let ultPosition = 0;
      let positionAtual = window.scrollY
      if(positionAtual > ultPosition){
        if(positionAtual > 2850){
          value ++
          container.style.opacity = `${value}`
        }
        if(positionAtual < 2800){
          container.style.opacity = "0"
        }
      }
    })
  }
}
//;
</script>
<style scoped>
.containerTestimonal{
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 40px 0px;
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

.containerGrid{
  opacity: 0;
  padding: 30px 10px;
  display: grid;
  grid-template-columns: repeat(3, 0.3fr);
  place-items: center;
  justify-content: center;
  align-items: start;
  transition: opacity 0.6s ease-in;
}

.card{
  width: 360px;
  border: 1px solid #D6BCFA;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  border-radius: 10px;
}
.headerCard{
  font-family: var(--fontPadrao);
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 5px;
}

.headerCard span{
  font-weight: 450;
}
.headerCard p{
  opacity: 0.6;
  font-weight: 400;
  font-size: 16px;
}

.bodyCard{
  margin-top: 8px;
  font-family: var(--fontPadrao);
  font-weight: 400;
  color: #532C59;
  font-size: 14px;
}

#ArieneMcCoy{
  position: relative;
  top: -20px;
}

#DianneRussell{
  position: relative;
  top: 20px;
}
#EleanorPena{
  position: relative;
  top: 30px;
}

@media screen and (max-width: 770px){
  .card{
    width: 230px !important;
    flex-wrap: wrap;
  }
  .containerGrid{
    grid-template-columns: repeat(3, 1fr) !important;
  }
  .containerTestimonal{
    margin-top: 60px;
  }
}

@media screen and (max-width: 376px){
  .containerGrid{
    grid-template-columns: repeat(1, 1fr) !important;
  }

  #DarleneRobertson, #JaneCooper, #EleanorPena, #LeslieAlexander, #ArieneMcCoy{
    display: none;
  }
  .containerTestimonal{
    margin-top: 230px;
  }
  .card{
    margin-top: 10px;
  }
  #DianneRussell{
    top: 0
  }
}
</style>
