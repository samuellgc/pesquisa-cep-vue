<template>
  <button class="btn">
    <span>{{ icon }}</span
    >{{ msg }}
  </button>
</template>
<script>
export default {
  name: "BtnMenu",
  props: {
    msg: String,
    icon: String,
  },
};
</script>
<style scoped>
.btn {
  min-width: 250px;
  height: 45px;
  background-color: #b600ee;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 16px 10px;
  border-radius: 8px;
  border: none;
  color: white;
  font-size: 16px;
  cursor: pointer;
  font-family: "Open Sans";
  font-style: normal;
  font-weight: 700;
}

.btn span {
  font-size: 30px;
  font-family: "Open Sans";
  font-style: normal;
  font-weight: 700;
  margin-right: 8px;
}
</style>