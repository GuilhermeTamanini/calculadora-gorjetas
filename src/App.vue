<script >
export default {
  data() {
    return {
      accountValue: 0,
      Tip: 15,
      peopleNumber: 1,
    };
  },
  methods: {
    calcular() {
      const accountValue = this.accountValue;

      const Tip = this.Tip;

      const peopleNumber = this.peopleNumber;

      let valueTip = 0;

      let valueTotal = {};

      valueTip = accountValue * (Tip / 100);

      valueTotal = (accountValue + valueTip) / peopleNumber;

      valueTotal = Math.round(valueTotal * 100) / 100;

      valueTotal = valueTotal.toFixed(2);

      console.log(valueTotal);

      document.getElementById("resultado").innerHTML = valueTotal;
    }
  }
  //K K K K K K K K K K K K K K K K K K K K K K KK K K K K K K K K K K K K K K K K K K K K K K KK K K KK  K KK K K KK K KK K K KK K KK K KK K K KK K KK K  KK K KK K K KK K KK K KK K  KK K KK 
};
</script>

<template>

  <div class="main">

    <h1><strong>Conta</strong></h1>

    <form>

      <label>
        <p>Qual o preço do jantar?</p>
        <input type="number" v-model="accountValue" id="accountValue">
      </label>

      <label>
        <p>Qual a Gorjeta? </p>
        <select v-model="Tip" id="valueTip">
          <option value="10000">Mundo das ideias</option>
          <option value="30">30% Mas bah </option>
          <option value="25">25% Muito bom</option>
          <option value="20">20% Bom</option>
          <option value="15">15% Aceitável</option>
          <option value="10">10% Ruim</option>
          <option value="5">5% "Nojo -_-"</option>
        </select>
      </label>

      <label>
        <p>Quantas pessoas vão dividir a Conta?</p>
        <input v-model="peopleNumber" type="number" id="peopleNumber" />
      </label>

      <label>
        <button type="button" @click="calcular">CALCULAR</button>
      </label>
      <label >
        <p>Valor</p>
        <span id="resultado">R$ 0.00</span>
      </label>

    </form>

  </div>

</template>

<style scoped>
*{
background-color: black;
color: white;
}
button {
  border: 1px solid red;
}
span {
  border: 1px solid red;
}
select {
  border:1px solid red;
}
div {
  text-align: center;
}
input {
  border: 1px solid red;
}
form label {
  margin: 20px;
  display: block;
}
form {
  width: 1500px;
  height: 1000px;
}
h1 {
  padding-right:80px ;
}
span {
  font-size:20px;
  padding: 10px;
}
</style>