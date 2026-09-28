# RN-006 — Conta Ativa para Operações

**Título:**  
Somente contas ativas podem realizar operações bancárias.

**Descrição:**  
Contas que estejam inativas, bloqueadas ou encerradas não devem realizar 
operações financeiras que alterem seu saldo.

**Origem:**  
Processo de controle da situação das contas bancárias.

**Stakeholders envolvidos:**  
Cliente, operador de suporte e administrador operacional.

**Condição:**  
Quando uma operação financeira for solicitada utilizando uma conta bancária.

**Regra:**  
O sistema deve verificar a situação da conta antes de efetivar uma operação. 
Somente contas com situação ativa podem realizar operações financeiras.

**Exceções:**  
Operações administrativas específicas podem ser realizadas em contas 
inativas, bloqueadas ou encerradas quando forem autorizadas pelo sistema.

**Dados envolvidos:**  
Conta bancária, identificador da conta, situação da conta e tipo da operação.

**Prioridade:**  
Alta

**Status:**  
Aprovado

**Requisitos relacionados:**  
RF-006

**Observações:**  
A verificação da situação da conta deve ocorrer antes da alteração de seu 
saldo.
