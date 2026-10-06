# RF-008 — Consulta de Saldo

**Título:**  
Consulta do saldo da conta.

**Descrição:**  
O sistema deve permitir que um cliente autenticado consulte o saldo disponível 
de sua conta.

**Objetivo:**  
Permitir que o cliente acompanhe o saldo disponível de sua conta bancária.

**Stakeholders:**  
Cliente.

**Ator principal:**  
Cliente.

**Pré-condições:**  
- O usuário deve estar autenticado.
- O usuário deve possuir uma conta cadastrada no sistema.

**Entradas:**  
Identificação do usuário e da conta.

**Processamento esperado:**  
O sistema deve identificar a conta associada ao usuário autenticado, consultar 
o saldo disponível e apresentar o valor ao cliente.

**Saídas/Resultados:**  
Saldo disponível da conta apresentado ao cliente.

**Pós-condições:**  
O saldo da conta deve permanecer inalterado após a consulta.

**Fluxos alternativos/exceções:**  
- Caso o usuário não esteja autenticado, o sistema deve impedir a consulta.
- Caso não exista uma conta associada ao usuário, o sistema deve informar que 
  não há conta disponível para consulta.

**Regras de negócio relacionadas:**  
RN-002

**Prioridade:**  
Alta

**Status:**  
Aprovado

**Critérios de aceite:**  
- O sistema deve permitir a consulta para um usuário autenticado.
- O sistema deve apresentar o saldo disponível da conta.
- O sistema não deve alterar o saldo durante a consulta.
- O sistema deve impedir a consulta quando o usuário não estiver autenticado.
- O sistema deve informar quando não existir uma conta associada ao usuário.

**Casos de uso relacionados:**  
UC-003

**Tarefas relacionadas:**  
TASK-XXX

**Casos de teste relacionados:**  
CT-XXX
