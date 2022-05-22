<template>
  <section class="card-dash">
    <div class="card-top">
      <div class="top-div-top">
        <p><InputDashboard /></p>
        <p><BtnMenu icon="+" msg="Adicionar endereço" /></p>
      </div>
      <div class="top-div-middle">
        <div class="cep">
          <img src="../assets/icone-lugar.svg" alt="" class="icone-cep" />
          <p>
            <span> CEP </span>
            60411-260
          </p>
        </div>
        <div class="cep">
          <img src="../assets/icone-lugar.svg" alt="" class="icone-cep" />
          <p>
            <span> CEP </span>
            60411-260
          </p>
        </div>
      </div>
      <div class="top-div-down">
        <div><BtnMenu msg="Gerar endereço" /></div>
      </div>
    </div>
    <div class="card-down"></div>
  </section>
</template>
<script>
import BtnMenu from "./BtnMenu.vue";
import InputDashboard from "./InputDashboard.vue";
export default {
  name: "DashboardMenu",
  components: {
    BtnMenu,
    InputDashboard,
  },
};
</script>
<style scoped>
.card-dash {
  margin: 30px 135px;
  min-height: 400px;
  width: 540px;
}

.card-top {
  min-height: 220px;
  width: 100%;
  padding-bottom: 20px;
  border-bottom: 1px solid #b7b7b7;
}

.top-div-top {
  height: 60px;
  width: 100%;
  display: flex;
  justify-content: space-between;
}

.top-div-middle {
  margin-top: 25px;
  margin-bottom: 40px;
  width: 100%;
}

.top-div-down {
  width: 100%;
  display: flex;
  justify-content: end;
  align-content: center;
}

.cep {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  margin-bottom: 10px;
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