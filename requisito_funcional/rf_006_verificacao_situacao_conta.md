## RF-006 — Verificação da Situação da Conta

**Título:**  
Verificação da situação da conta antes de operações.

**Descrição:**  
O sistema deve verificar se a conta está ativa antes de permitir operações 
financeiras que alterem seu saldo.

**Objetivo:**  
Impedir movimentações financeiras em contas que estejam inativas, bloqueadas 
ou encerradas.

**Stakeholders:**  
Cliente, operador de suporte e administrador operacional.

**Ator principal:**  
Cliente ou operador autorizado.

**Pré-condições:**  
- O usuário deve estar autenticado.
- Uma operação financeira deve ter sido solicitada.
- A conta envolvida deve estar cadastrada no sistema.

**Entradas:**  
Identificação da conta, situação da conta e tipo da operação.

**Processamento esperado:**  
O sistema deve consultar a situação da conta e permitir a operação somente 
quando a conta estiver ativa.

**Saídas/Resultados:**  
Operação autorizada para processamento ou mensagem indicando que a conta não 
está disponível para a operação.

**Pós-condições:**  
Uma conta ativa pode prosseguir com a operação. Uma conta inativa, bloqueada 
ou encerrada não deve ter seu saldo alterado pela operação.

**Fluxos alternativos/exceções:**  
Operações administrativas autorizadas podem ser realizadas em contas que não 
estejam ativas, conforme as permissões e regras específicas do sistema.

**Regras de negócio relacionadas:**  
RN-006

**Prioridade:**  
Alta

**Status:**  
Aprovado

**Critérios de aceite:**  
- O sistema deve permitir operações em contas ativas.
- O sistema deve impedir operações financeiras em contas inativas.
- O sistema deve impedir operações financeiras em contas bloqueadas.
- O sistema deve impedir operações financeiras em contas encerradas.
- O sistema não deve alterar o saldo de uma conta impedida de realizar a 
  operação.

**Casos de uso relacionados:**  
UC-XXX

**Tarefas relacionadas:**  
TASK-XXX

**Casos de teste relacionados:**  
CT-XXX
