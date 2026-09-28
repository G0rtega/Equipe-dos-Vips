# RN-007 — Consulta do Histórico de Transações

**Título:**  
Consulta do histórico de transações da conta.

**Descrição:**  
O sistema deve permitir que usuários autenticados consultem o histórico de 
transações das contas às quais possuem acesso.

**Origem:**  
Processo de consulta e acompanhamento das movimentações bancárias.

**Stakeholders envolvidos:**  
Cliente, operador de suporte e administrador operacional.

**Condição:**  
Quando um usuário autenticado solicitar o histórico de movimentações de uma 
conta.

**Regra:**  
O sistema deve apresentar as transações associadas à conta consultada, 
contendo as informações necessárias para identificar cada operação, como tipo, 
valor, data e contas envolvidas.

**Exceções:**  
Um usuário não deve visualizar o histórico de uma conta à qual não possui 
permissão de acesso.

**Dados envolvidos:**  
Usuário, conta bancária, transações, tipo da operação, valor, data e hora, 
conta de origem, conta de destino e status da transação.

**Prioridade:**  
Média

**Status:**  
Aprovado

**Requisitos relacionados:**  
RF-007

**Observações:**  
A consulta deve respeitar as regras de autenticação e autorização definidas 
pelo sistema.
