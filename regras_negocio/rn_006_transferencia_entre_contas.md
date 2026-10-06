# RN-006 — Transferência entre Contas

**Título:**  
Transferências devem possuir origem e destino válidos.

**Descrição:**  
Uma transferência bancária deve ser realizada entre contas válidas, com o 
valor sendo debitado da conta de origem e creditado na conta de destino.

**Origem:**  
Processo de transferência de valores entre contas bancárias.

**Stakeholders envolvidos:**  
Cliente e operador de suporte.

**Condição:**  
Quando um usuário solicitar uma transferência de valores entre duas contas.

**Regra:**  
O sistema deve validar as contas de origem e destino e verificar se a conta 
de origem possui saldo suficiente para a operação. Após a validação, o sistema 
deve debitar o valor da conta de origem e creditá-lo na conta de destino.

**Exceções:**  
Transferências não devem ser realizadas quando a conta de origem ou destino 
for inválida ou quando o saldo disponível da conta de origem for insuficiente.

**Dados envolvidos:**  
Conta de origem, conta de destino, valor da transferência e saldo disponível.

**Prioridade:**  
Crítica

**Status:**  
Aprovado

**Requisitos relacionados:**  
RF-006

**Observações:**  
A transferência deve ser tratada como uma única operação, evitando que apenas 
o débito ou apenas o crédito seja efetivado.
