<script>

function TestaCPF(strCPF) {
    var Soma;
    var Resto;
    Soma = 0;
  if (strCPF == "00000000000") return false;
     
  for (i=1; i<=9; i++) Soma = Soma + parseInt(strCPF.substring(i-1, i)) * (11 - i);
  Resto = (Soma * 10) % 11;
   
    if ((Resto == 10) || (Resto == 11))  Resto = 0;
    if (Resto != parseInt(strCPF.substring(9, 10)) ) return false;
   
  Soma = 0;
    for (i = 1; i <= 10; i++) Soma = Soma + parseInt(strCPF.substring(i-1, i)) * (12 - i);
    Resto = (Soma * 10) % 11;
   
    if ((Resto == 10) || (Resto == 11))  Resto = 0;
    if (Resto != parseInt(strCPF.substring(10, 11) ) ) return false;
    return true;
}
var strCPF = "12345678909";
alert(TestaCPF(strCPF));


</script>

<template>
  <div>
    <form class="cf">
      <h1>Cadastro de Cliente</h1>
        <div class="half left cf">
          <input type="text" id="input-name" placeholder="Nome Completo">
          <input type="text" id="input-cpf" placeholder="CPF">
          <input type="text" id="input-cep" placeholder="CEP">
          <input type="text" id="input-endereco" placeholder="Endereço">
        </div>
      <input type="submit" value="Submit" id="input-submit">
    </form>
  </div>
</template> 


<style src="./style.css"></style>
