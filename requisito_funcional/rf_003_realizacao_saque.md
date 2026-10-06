# RF-003 — Realização de Saque

**Título:**  
Realização de saque em conta bancária.

**Descrição:**  
O sistema deve permitir que um cliente realize um saque quando o valor 
solicitado não exceder o saldo disponível da conta.

**Objetivo:**  
Permitir a retirada de valores de uma conta bancária mantendo o controle 
correto do saldo disponível.

**Stakeholders:**  
Cliente e operador de suporte.

**Ator principal:**  
Cliente.

**Pré-condições:**  
- O usuário deve estar autenticado.
- A conta deve existir no sistema.

**Entradas:**  
Identificação da conta e valor do saque.

**Processamento esperado:**  
O sistema deve validar se o valor do saque é maior que zero e verificar se há 
saldo suficiente na conta. Quando a operação for válida, deve descontar o valor 
do saque do saldo da conta e registrar a transação.

**Saídas/Resultados:**  
Saque efetivado e saldo da conta atualizado.

**Pós-condições:**  
O saldo da conta deve ser reduzido pelo valor do saque e a transação deve 
estar registrada no histórico.

**Fluxos alternativos/exceções:**  
- Caso o saldo seja insuficiente, o saque não deve ser realizado.
- Caso o valor seja igual ou inferior a zero, o saque não deve ser realizado.

**Regras de negócio relacionadas:**  
RN-003, RN-004, RN-005

**Prioridade:**  
Alta

**Status:**  
Aprovado

**Critérios de aceite:**  
- O sistema deve realizar o saque quando o valor for positivo e houver saldo 
  suficiente.
- O sistema deve impedir o saque quando o saldo for insuficiente.
- O sistema deve impedir o saque quando o valor for igual ou inferior a zero.
- O sistema deve atualizar o saldo após um saque válido.
- O sistema deve registrar um saque efetivado.

**Casos de uso relacionados:**  
UC-004

**Tarefas relacionadas:**  
TASK-XXX

**Casos de teste relacionados:**  
CT-XXX
