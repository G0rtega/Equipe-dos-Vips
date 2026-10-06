# RF-007 — Consulta do Histórico de Transações

**Título:**  
Consulta do histórico de transações da conta.

**Descrição:**  
O sistema deve permitir que usuários autenticados consultem o histórico de 
transações das contas às quais possuem acesso.

**Objetivo:**  
Permitir que os usuários acompanhem as movimentações financeiras realizadas 
em suas contas.

**Stakeholders:**  
Cliente e operador de suporte.

**Ator principal:**  
Cliente.

**Pré-condições:**  
- O usuário deve estar autenticado.
- O usuário deve possuir permissão para consultar a conta.
- A conta deve existir no sistema.

**Entradas:**  
Identificação da conta e identificação do usuário.

**Processamento esperado:**  
O sistema deve verificar a permissão de acesso do usuário e, quando autorizada, 
deve recuperar as transações associadas à conta e apresentá-las ao usuário.

**Saídas/Resultados:**  
Histórico das transações da conta, contendo informações como tipo, valor, 
data, hora, origem e destino, quando aplicável.

**Pós-condições:**  
O usuário deve conseguir visualizar as transações às quais possui permissão 
de acesso.

**Fluxos alternativos/exceções:**  
- Caso o usuário não esteja autenticado, o acesso ao histórico deve ser negado.
- Caso o usuário não possua permissão para consultar a conta, o acesso deve 
  ser negado.
- Caso não existam transações para a conta, o sistema deve informar que não 
  há movimentações registradas.

**Regras de negócio relacionadas:**  
RN-002, RN-004, RN-007

**Prioridade:**  
Média

**Status:**  
Aprovado

**Critérios de aceite:**  
- O sistema deve permitir a consulta para usuários autenticados e autorizados.
- O sistema deve impedir a consulta de contas sem permissão de acesso.
- O sistema deve apresentar as transações associadas à conta.
- O sistema deve apresentar as informações necessárias para identificar cada 
  transação.
- O sistema deve informar quando não houver transações registradas.

**Casos de uso relacionados:**  
UC-006

**Tarefas relacionadas:**  
TASK-XXX

**Casos de teste relacionados:**  
CT-XXX
