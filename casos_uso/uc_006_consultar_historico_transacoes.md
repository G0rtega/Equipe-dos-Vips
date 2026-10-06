# UC-006 — Consultar Histórico de Transações

**Ator principal:**  
Cliente.

**Objetivo:**  
Permitir que o cliente consulte as transações realizadas em sua conta.

**Pré-condições:**
- O cliente deve estar autenticado.
- O cliente deve possuir uma conta.
- O cliente deve possuir permissão para consultar a conta.

**Pós-condições:**
- O histórico de transações é apresentado ao cliente.
- Nenhum dado financeiro da conta é alterado.

**Requisitos relacionados:**  
RF-004, RF-007

**Regras de negócio relacionadas:**  
RN-002, RN-004, RN-007

**RNFs relacionados:**  
RNF-001, RNF-002

**Fluxo principal:**

1. O cliente acessa a funcionalidade de histórico.
2. O sistema identifica o cliente autenticado.
3. O sistema identifica a conta associada ao cliente.
4. O sistema verifica a permissão de acesso.
5. O sistema consulta as transações da conta.
6. O sistema apresenta o histórico ao cliente.
7. O cliente pode consultar os detalhes de uma transação.

**Fluxos alternativos/exceções:**

- **FA-001 — Cliente não autenticado:**  
  Caso o cliente não esteja autenticado, o sistema deve impedir o acesso ao 
  histórico.

- **FA-002 — Acesso não autorizado:**  
  Caso o cliente não possua permissão para consultar a conta, o sistema deve 
  negar o acesso.

- **FA-003 — Nenhuma transação:**  
  Caso não existam transações registradas, o sistema deve informar que não há 
  movimentações disponíveis.

**Resultado:**  
Histórico das transações da conta apresentado ao cliente.

**Rastreabilidade:**  
RN-002 → RF-007 → UC-006 → CT-XXX  
RN-004 → RF-004 → UC-006 → CT-XXX  
RN-007 → RF-007 → UC-006 → CT-XXX
