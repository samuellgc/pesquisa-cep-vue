<template>
  <section class="card-dash">
    <div class="card-top">
      <div class="top-div-top">
        <p>
          <input
            type="text"
            v-model="info"
            class="input-cep"
            name="cep"
            id="cep"
            placeholder="Insira seu CEP"
          />
        </p>
        <p>
          <BtnMenu icon="+" msg="Adicionar endereço" v-on:click="insertCep()" />
        </p>
      </div>
      <div class="top-div-middle">
        <div v-for="cep in ceps" :key="cep" class="div-cep">
          <CardCep :cep="cep" />
        </div>
      </div>
      <div class="top-div-down">
        <div>
          <BtnMenu msg="Gerar endereço" v-on:click="getEnd()" />
        </div>
      </div>
    </div>
    <div
      class="card-down"
      :id="endereco.siafi"
      v-for="endereco in enderecos"
      :key="endereco.siafi"
    >
      <CardDash
        :logradouro="endereco.logradouro"
        :cep="endereco.cep"
        :localidade="endereco.localidade"
        :uf="endereco.uf"
        v-on:click="removeCep()"
      />
    </div>
  </section>
</template>
<script>
import BtnMenu from "./BtnMenu.vue";
import axios from "axios";
import CardCep from "./CardCep.vue";
import CardDash from "./CardDash.vue";
export default {
  name: "DashboardMenu",
  components: {
    BtnMenu,
    CardCep,
    CardDash,
  },
  data() {
    return {
      info: null,
      ceps: [],
      enderecos: [],
      baseUrl: "https://viacep.com.br/ws/",
    };
  },
  methods: {
    getEnd() {
      for (this.cep of this.ceps) {
        var url = `${this.baseUrl}${this.cep}/json/`;
      }
      axios
        .get(url)
        .then((res) => {
          this.enderecos.push(res.data);
          console.log(this.enderecos);
          this.limparInput()
        })
        .catch((error) => {
          console.log(error);
        });
    },

    insertCep() {
      this.ceps.push(this.info);
      console.log(this.ceps);
      this.info = '';
    },

    removeCep() {
      for (this.cep in this.ceps) {
        this.ceps.splice(this.cep, 1);
      }
      for (this.endereco in this.enderecos) {
        this.enderecos.splice(this.endereco, 1);
      }
    },
  },
};
</script>
<style scoped>
.card-dash {
  margin: 30px 135px;
  min-height: 400px;
  width: 540px;
}

.div-cep {
  margin-bottom: 15px;
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
  min-height: 70px;
  margin-top: 25px;
  margin-bottom: 40px;
  width: 100%;
}

.top-div-down {
  width: 100%;
  justify-content: end;
  align-content: center;
  display: flex;
}

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