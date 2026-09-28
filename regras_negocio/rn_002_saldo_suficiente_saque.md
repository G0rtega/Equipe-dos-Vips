# RN-002 — Saldo Suficiente para Saque

**Título:**  
Saque permitido somente quando houver saldo suficiente.

**Descrição:**  
O sistema não deve permitir que um cliente realize um saque cujo valor seja 
superior ao saldo disponível em sua conta.

**Origem:**  
Processo de movimentação financeira e controle de saldo das contas bancárias.

**Stakeholders envolvidos:**  
Cliente, operador de suporte e administrador operacional.

**Condição:**  
Quando um cliente ou operador autorizado solicitar um saque em uma conta 
bancária.

**Regra:**  
O sistema deve verificar o saldo disponível antes de efetivar o saque. O valor 
do saque não pode ser superior ao saldo disponível na conta. Quando a operação 
for válida, o valor deve ser descontado do saldo da conta.

**Exceções:**  
Contas ou modalidades que possuam limite de crédito ou cheque especial podem 
permitir operações acima do saldo disponível, conforme as regras específicas 
desse produto.

**Dados envolvidos:**  
Conta bancária, saldo disponível, valor do saque, limite de crédito e situação 
da conta.

**Prioridade:**  
Alta

**Status:**  
Aprovado

**Requisitos relacionados:**  
RF-002

**Observações:**  
A verificação do saldo deve ocorrer antes da efetivação da operação para evitar 
que a conta fique com saldo inválido.
