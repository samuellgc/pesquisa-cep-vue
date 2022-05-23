<template>
  <div class="cep">
    <img src="../assets/icone-lugar.svg" alt="" class="icone-cep" />
    <p>
      <span> CEP </span>
      {{ cep }}
    </p>
  </div>
</template>
<script>
export default {
  name: "CardCep",
  props: {
    cep: String,
  },
};
</script>
<style scoped>
.cep {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  margin-bottom: 5px;
}

.icone-cep {
  height: 22px;
  margin-right: 15px;
}

.cep p {
  align-items: center;
  font-family: "Open Sans";
  color: gray;
}

.cep p span {
  font-family: "Open Sans";
  font-weight: 700;
  color: #20272c;
}
</style>