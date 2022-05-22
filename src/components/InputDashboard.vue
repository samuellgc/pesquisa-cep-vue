<template>
  <input type="text" class="input-cep" placeholder="Insira seu CEP" />
</template>
<script>
export default {
  name: "InputDashboard",
};
</script>
<style scoped>
.input-cep {
  min-width: 250px;
  height: 45px;
  border: 2px solid #bbc4ce;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding: 16px;
  box-sizing: border-box;
  border-radius: 10px;
}

::-webkit-input-placeholder {
  font-family: "Open Sans";
  font-weight: 400;
  size: 16px;
}

:-ms-input-placeholder {
  font-family: "Open Sans";
  font-weight: 400;
  size: 16px;
}
</style>