<template>
  <section class="side-bar">
    <div class="div-i">
      <img src="../assets/icone-busca.svg" alt="Ícone lupa" class="i-size" />
      <img src="../assets/icone-folder2.svg" alt="Ícone pasta" class="i-size" />
    </div>
    <div>
      <img src="../assets/icone-ajuste.svg" alt="Ícone ajuste" class="i-ajuste" />
    </div>
  </section>
</template>
<script>
export default {
  name: "SideMenu",
};
</script>
<style scoped>
.side-bar {
  height: 100%;
  width: 7%;
  background-color: #f7f7f7;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0;
}

.i-ajuste {
    background: #20272C;
    border-radius: 10px;
    padding: 8px;
}

.div-i {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    gap: 60px;
    margin-top: 30px;
}

</style>