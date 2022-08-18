<script>
export default {
  name: 'WeatherApp',
  data() {
      return {
            valor: 0,
          
          }
  }
  }
</script>

<template>
  <main>
    {{valor}}
    <div class="painel">
      <h3>Calculadora de Gorjetas</h3>
      <label for="">Qual o valor da conta?</label>
      <input type="text" v-model="valor"/>
      <label for="">Como foi o serviço?</label>
      <select data-v-7b896a00="">
        <option value="30" data-v-7b896a00="">30% (Excepcional)</option>
        <option value="25" data-v-7b896a00="">25% (Mais do que bom)</option>
        <option value="20" data-v-7b896a00="">20% (Bom)</option>
        <option value="15" data-v-7b896a00="">15% (OK)</option>
        <option value="10" data-v-7b896a00="">10% (Ruim)</option>
        <option value="5" data-v-7b896a00="">5% (Péssimo)</option>
      </select>
      <label for="">Quantas pessoas estão pagando a conta?</label>
      <input type="number" name="" id="" />
    </div>
  </main>
</template>
<style scoped>
main {
  min-height: 100vh;
  display: flex;
  place-items: center;
  align-items: center;
  justify-content: center;
}
.painel {
  background-color: rgb(214, 214, 214);
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 15px;
  padding: 30px;
}
input,
select {
  max-width: 240px;
}
</style>
