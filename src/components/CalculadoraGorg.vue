<script>
export default {
  name: 'WeatherApp',
  data() {
    return {
      valor: 0,
      taxa: 0,
      qtdPessoas: 1
    }
  },

  computed: {
    // a computed getter
    total() {
      // `this` points to the component instance
      return this.total = ((parseFloat(this.valor) * parseFloat(this.taxa)) + parseFloat(this.valor)).toFixed(2)
    },
    totalPorPessoa() {
      // `this` points to the component instance
      return this.totalPorPessoa = (((parseFloat(this.valor) * parseFloat(this.taxa)) + parseFloat(this.valor)) / parseInt(this.qtdPessoas)).toFixed(2)
    }
  }
}
</script>
<template>
  <main>
    <div class="painel">
      <h3>Calculadora de Gorjetas</h3>
      <label for="" class="infos">Qual o valor da conta?</label>
      <input type="text" v-model="valor" id="totalconta" />
      <label for="" class="infos">Como foi o serviço?</label>
      <select data-v-7b896a00="" id="taxa" v-model="taxa">
        <option value="0.30" data-v-7b896a00="">30% (Excepcional)</option>
        <option value="0.25" data-v-7b896a00="">25% (Mais do que bom)</option>
        <option value="0.20" data-v-7b896a00="">20% (Bom)</option>
        <option value="0.15" data-v-7b896a00="">15% (OK)</option>
        <option value="0.10" data-v-7b896a00="">10% (Ruim)</option>
        <option value="0.05" data-v-7b896a00="">5% (Péssimo)</option>
      </select>
      <label for="" class="infos">Quantas pessoas estão pagando a conta?</label>
      <input type="number" name="" id="qntsP" v-model="qtdPessoas"/>
      <span>Sua Conta ficou R$: {{ total }} por pessoa {{ totalPorPessoa }}</span>
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
