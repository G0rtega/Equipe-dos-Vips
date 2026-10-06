# RF-006 — Realização de Transferência

**Título:**  
Transferência de valores entre contas bancárias.

**Descrição:**  
O sistema deve permitir a transferência de valores entre uma conta de origem 
e uma conta de destino válidas, desde que a conta de origem possua saldo 
suficiente.

**Objetivo:**  
Permitir a movimentação de valores entre contas bancárias de forma controlada.

**Stakeholders:**  
Cliente.

**Ator principal:**  
Cliente.

**Pré-condições:**  
- O usuário deve estar autenticado.
- A conta de origem deve existir no sistema.
- A conta de destino deve existir no sistema.

**Entradas:**  
Conta de origem, conta de destino e valor da transferência.

**Processamento esperado:**  
O sistema deve validar as contas e o valor da transferência, verificar o 
saldo disponível da conta de origem e, caso todas as condições sejam atendidas, 
debitar o valor da conta de origem, creditar o mesmo valor na conta de destino 
e registrar a transação.

**Saídas/Resultados:**  
Transferência efetivada, saldo das contas atualizado e transação registrada.

**Pós-condições:**  
O saldo da conta de origem deve ser reduzido pelo valor transferido, o saldo 
da conta de destino deve ser aumentado pelo mesmo valor e a transação deve 
estar registrada.

**Fluxos alternativos/exceções:**  
- Caso a conta de origem seja inválida, a transferência não deve ser realizada.
- Caso a conta de destino seja inválida, a transferência não deve ser realizada.
- Caso o saldo seja insuficiente, a transferência não deve ser realizada.
- Caso o valor seja igual ou inferior a zero, a transferência não deve ser 
  realizada.
- Caso ocorra uma falha durante a operação, o débito e o crédito não devem ser 
  efetivados parcialmente.

**Regras de negócio relacionadas:**  
RN-004, RN-005, RN-006

**Prioridade:**  
Crítica

**Status:**  
Aprovado

**Critérios de aceite:**  
- O sistema deve validar a conta de origem antes da transferência.
- O sistema deve validar a conta de destino antes da transferência.
- O sistema deve verificar o saldo disponível da conta de origem.
- O sistema deve impedir transferências com valor igual ou inferior a zero.
- O sistema deve debitar a conta de origem quando a transferência for válida.
- O sistema deve creditar a conta de destino quando a transferência for válida.
- O sistema deve registrar a transferência efetivada.
- O sistema não deve realizar apenas o débito ou apenas o crédito em caso de 
  falha na operação.

**Casos de uso relacionados:**  
UC-005

**Tarefas relacionadas:**  
TASK-XXX

**Casos de teste relacionados:**  
CT-XXX
