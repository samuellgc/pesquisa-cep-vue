<template>
  <div class="card_dash">
    <div class="card_dash_end">
      <img src="../assets/icone-lugar.svg" alt="" class="icone-dash-cep" />
      <div>
        <p class="card-dash-logra">{{ logradouro }}</p>
        <p>{{ localidade }} - {{ uf }}</p>
      </div>
    </div>
    <div class="card_dash_cep">
      <div class="card-dash-cep">{{ cep }}</div>
      <img src="../assets/icone-lixo.svg" alt="" class="icone-lixo" @click="deleteCard"/>
    </div>
  </div>
</template>
<script>
export default {
  name: "CardDash",
  props: {
      logradouro: String,
      localidade: String,
      uf: String,
      cep: String,
      deleteCard: Function
  }
};
</script>
<style scoped>
.card_dash,
.card_dash_end,
.card_dash_cep {
  display: flex;
  justify-content: space-between;
  align-content: center;
}

.card_dash_end div {
    align-self: center;
}

.card_dash {
  padding: 15px 10px;
  box-shadow: 0px 4px 20px rgba(32, 39, 44, 0.1);
  border-radius: 8px;
  margin: 20px 0 10px 0;
}

.icone-lixo {
    height: 16.5px;
    align-self: center;
    cursor:pointer;
    padding: 15px 0;
}

.card_dash_cep div {
  min-width: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 30px 10px;
  margin-right: 10px;
  color: #B600EE;
  border-right: 2px solid #E0E6EA;
}

.icone-dash-cep {
  height: 22px;
  margin-right: 10px;
  align-self: center;
}

.card-dash-cidade,
.card-dash-cep {
  font-family: "Open sans";
  font-weight: 400;
  font-size: 16px;
}

.card-dash-logra {
  font-family: "Open sans";
  font-weight: 700;
  font-size: 20px;
}
</style>