# RN-003 — Saldo Suficiente para Saque

**Título:**  
Saque permitido somente quando houver saldo suficiente.

**Descrição:**  
O sistema não deve permitir que um cliente realize um saque cujo valor seja 
superior ao saldo disponível em sua conta.
# RN-003 — Saldo Suficiente para Saque

**Título:**  
Saque permitido somente quando houver saldo suficiente.

**Descrição:**  
O sistema não deve permitir que um cliente realize um saque cujo valor seja 
superior ao saldo disponível em sua conta.

**Origem:**  
Processo de movimentação financeira e controle de saldo das contas bancárias.

**Stakeholders envolvidos:**  
Cliente e operador de suporte.

**Condição:**  
Quando um cliente solicitar um saque em sua conta bancária.

**Regra:**  
O sistema deve verificar o saldo disponível antes de efetivar o saque. O valor 
do saque não pode ser superior ao saldo disponível na conta. Quando a operação 
for válida, o valor deve ser descontado do saldo da conta.

**Exceções:**  
O saque deve ser rejeitado quando o valor solicitado for superior ao saldo 
disponível na conta.

**Dados envolvidos:**  
Conta bancária, saldo disponível e valor do saque.
