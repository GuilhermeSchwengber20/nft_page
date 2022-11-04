<template>
  <div class="containerHeader">
    <div class="menu">
      <a>Home</a>
      <a>University</a>
      <a>Courses</a>
    </div>
    <div class="logo">
      <img src="../assets/img/Logo.png" />
    </div>
    <div class="menu">
      <a>Use cases</a>
      <a>Plans</a>
      <a>Resources</a>
    </div>
  </div>
</template>
<script>
export default{
  name:"Header"
}
</script>
<style scoped>
.containerHeader{
  font-family: var(--fontPadrao);
  padding: 10px 0px;
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  gap: 50px;
  border-bottom: 1px solid #F8E0FB;
}

.menu a{
  margin-left: 20px;
}

@media screen and (max-width: 769px){
.menu a{
    white-space: nowrap;
    margin-left: 10px;
  }
}

@media screen and (max-width: 376px){
  .menu{
    display: none;
  }
}
</style>
