<template>
  <div class="containerFAQ">
    <div class="containerText">
      <div class="title">
        <h2>Frequently Asked Questions</h2>
      </div>
      <div class="text">
        <p>Risus commodo id odio turpis pharetra elementum. Pulvinar porta porta feugiat scelerisque in elit. Morbi rhoncus, tellus, eros consequat magna semper orci a tincidunt. </p>
      </div>
    </div>
    <div class="containerAskly">
      <div class="card">
        <p>What kind of websites I can build with Zeus UI?</p>
        <img src="../assets/img/angle-down.png" />
      </div>
      <div class="card">
        <p>Can I use Zeus UI in commercial projects?</p>
        <img src="../assets/img/angle-down.png" />
      </div>
      <div class="card">
        <p>Can I resell Zeus UI?</p>
        <img src="../assets/img/angle-down.png" />
      </div>
      <div class="card">
        <p>Could you make me a website using Zeus UI?</p>
        <img src="../assets/img/angle-down.png" />
      </div>
      <div class="cardOpen">
        <div class="cardHeader">
          <p>How much does Zeus UI cost?</p>
          <img src="../assets/img/angle-down.png" />
        </div>
        <div class="text">
          <p>This FAQ section is now in the expanded state, so you see how it looks. Rhoncus sed facilisi sed amet. Tristique commodo sodales.</p>
        </div>
      </div>
      <div class="card">
        <p>How long will you support Zeus UI?</p>
        <img src="../assets/img/angle-down.png" />
      </div>
      <div class="card">
        <p>WIs that easy to design a website with Zeus UI?</p>
        <img src="../assets/img/angle-down.png" />
      </div>
    </div>
  </div>
</template>
<script>
export default{
  name: "FAQSection"
}
</script>
<style scoped>
.containerFAQ{
  display: flex;
  flex-direction: row;
  justify-content: center;
  width: 100%;
  padding: 120px 20px;
  gap: 30px;
}
.containerText{
  width: 28%;
}

.containerText .title h2{
  font-family: var(--fontTitle);
  font-weight: 700;
  font-size: 36px;
  letter-spacing: 2px;
}

.containerText .text p{
  font-family: var(--fontPadrao);
  font-weight: 400;
  font-size: 14px;
  margin-top: 20px;
}
.containerAskly{
  width: 60%;
  display: grid;
  grid-template-columns: repeat(2, 0.4fr);
  column-gap: 10px;
}

.card{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
  align-self: stretch;
  width: 380px;
  border: 1px solid #D6BCFA;
  border-radius: 12px;
  height: 100px;
  padding: 20px;
  margin-top: 10px;
}

.cardOpen{
  display: flex;
  flex-direction: column;
  width: 380px;
  border: 1px solid #D6BCFA;
  border-radius: 12px;
  padding: 20px;
  background-color: #FFFFFF;
  margin-top: 10px;
}

.cardOpen p{
  font-family: var(--fontPadrao);
  font-weight: 600;
}
.cardOpen .cardHeader{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: start;
}
.cardOpen .text p{
  margin-top: 5px;
  font-weight: 300 !important;
  font-size: 14px;
}
.card p{
  font-family: var(--fontPadrao);
  font-weight: 600;
}
.card img{
  max-width: 40px;

}

@media screen and (max-width: 770px){
  .containerAskly{
    grid-template-columns: repeat(1, 0.4fr);
  }
  .containerFAQ{
    justify-content: space-between;
  }

  .containerText{
    width: 50%;
  }
  .containerText .title h2{
    font-family: var(--fontTitle);
    font-weight: 700;
    font-size: 30px;
    letter-spacing: 2px;
  }

}

@media screen and (max-width: 770px){
  .containerFAQ{
    display: flex;
    flex-direction: column;
    margin-top: 120px;
    text-align: center;
  }
  .containerText{
    width: 100%;
  }
  .card{
    width: 300px;
  }
  .cardOpen{
    width: 300px;
  }
}

</style>
