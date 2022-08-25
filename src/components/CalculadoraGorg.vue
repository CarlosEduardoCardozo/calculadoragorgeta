<script>
export default {
  name: 'WeatherApp',
  data() {
    return {
      valor: 0,

    }
  }
}
function ValorFinal() {
  let totalconta = document.getElementById("totalconta").value;
  let taxa = document.getElementById("taxa").value;
  let qntsP = document.getElementById("qntsP").value;

  if (totalconta === "" || taxa == 0 || isNaN(totalconta) || isNaN(qntsP)) {
    alert("Por favor, coloque um valor válido!");
    return;
  }


  var totalTaxaServico = (totalconta * taxa) / qntsP;
  var total = totalTaxaServico + (totalconta / qntsP);

  total = Math.round(total * 100) / 100;
  total = total.toFixed(2);

  return document.getElementById("valor-por-cabeca").innerHTML = total;
}


</script>

<template>
  <main>
    {{ total }}
    <div class="painel">
      <h3>Calculadora de Gorjetas</h3>
      <label for="" class="infos">Qual o valor da conta?</label>
      <input type="text" v-model="valor" id="totalconta" />
      <label for="" class="infos">Como foi o serviço?</label>
      <select data-v-7b896a00="" id="taxa">
        <option value="0.30" data-v-7b896a00="">30% (Excepcional)</option>
        <option value="0.25" data-v-7b896a00="">25% (Mais do que bom)</option>
        <option value="0.20" data-v-7b896a00="">20% (Bom)</option>
        <option value="0.15" data-v-7b896a00="">15% (OK)</option>
        <option value="0.10" data-v-7b896a00="">10% (Ruim)</option>
        <option value="0.05" data-v-7b896a00="">5% (Péssimo)</option>
      </select>
      <label for="" class="infos">Quantas pessoas estão pagando a conta?</label>
      <input type="number" name="" id="qntsP" />
      <span>Sua Conta ficou R$: por pessoa</span>
    </div>
  </main>
</template>
<style scoped>
* {
  padding: 0;
}

main {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: rgb(0, 76, 82);
}

.painel {
  background-color: rgba(0, 0, 0, 0.775);
  height: 300px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  margin: 15px;
  padding: 50px;
  color: #fff;
}

.infos,
h3, span {
  padding: 8px;
  font-family: Arial, Helvetica, sans-serif;
}

h3 {
  font-size: 1.5rem;
  color: rgb(61, 223, 196);
}

input,
select {
  max-width: 240px;
  padding: 8px;
  outline: 0;
  border-style: none;
  border-radius: 24px;
}
</style>
