<template>
  <nav class="nav-header">
    <div class="nav-first">
      <img src="../assets/logo.svg" alt="Logo empresa" />
      <div class="card-header">
        <p class="p-sp">Surreal São Paulo</p>
        <p class="p-vtex">VTEX</p>
      </div>
    </div>
    <div class="nav-last">
      <img src="../assets/icone-bell.svg" alt="Ícone sino" class="i-sino" />
      <p class="name-user">Olá, Joaquim</p>
      <img src="../assets/usuario.svg" alt="Ícone usuário" />
    </div>
  </nav>
</template>
<script>
export default {
  name: "NavMenu",
};
</script>
<style scoped>
.nav-header,
.nav-first,
.nav-last {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 25px;
}

.nav-last {
  margin-right: 25px;
}

.nav-first,
.nav-last {
  height: 50px;
  padding: 8px 20px;
}

.nav-header {
  background-color: #9206e9;
  color: white;
  height: 70px;
  padding: 5px 0;
}

.i-sino {
  padding: 25px 23px;
  border-right: 2px solid rgba(255, 255, 255, 0.2);
}

.card-header {
  border: 2px solid white;
  padding: 6px 130px 6px 10px;
  border-radius: 10px;
}

.p-sp,
.p-vtex,
.name-user {
  font-family: "Open Sans";
}

.p-sp,
.name-user {
  font-weight: 700;
  size: 16px;
}

.p-vtex {
  font-weight: 400;
  size: 12px;
}
</style>