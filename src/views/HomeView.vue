<script setup>
</script>

<template>
  <div class="calculadora">
  <h3> Calculadora de gorjetas </h3>
  <div class="valor">Valor da conta
    <div><input type="number"></div>
  </div>
  <div class="valor">Como foi nosso atendimento?
    <div><select name="15%(OK)" id=""> 
      <option value="30">30%(Excepcional)</option>
      <option value="25">25%(Mais do que bom)</option>
      <option value="20">20%(Bom)</option>
      <option value="15">15%(OK)</option>
      <option value="10">10%(ruin)</option>
      <option value="5">5%(Péssimo)</option>
      
      </select></div>
  </div>
  </div>
</template>
<style>
#valor {
  margin: 15px;
}
.calculadora {
  justify-content: center;
  text-align: center;
  padding-top:100px ;
}
select {
  height: 30px;
  width: 256px;
}
</style>