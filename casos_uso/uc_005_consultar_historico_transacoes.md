# UC-005 — Consultar Histórico de Transações

**Ator principal:**  
Cliente

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
RF-003, RF-007

**Regras de negócio relacionadas:**  
RN-001, RN-003, RN-007

**RNFs relacionados:**  
RNF-001, RNF-002, RNF-005

**Fluxo principal:**

1. Cliente acessa a funcionalidade de histórico.
2. Sistema identifica o cliente autenticado.
3. Sistema identifica a conta associada ao cliente.
4. Sistema verifica a permissão de acesso.
5. Sistema consulta as transações da conta.
6. Sistema apresenta o histórico ao cliente.
7. Cliente pode consultar os detalhes de uma transação.

**Fluxos alternativos/exceções:**

- **FA-001 — Cliente não autenticado:**  
  Caso o cliente não esteja autenticado, o sistema deve impedir o acesso ao histórico.

- **FA-002 — Acesso não autorizado:**  
  Caso o cliente não possua permissão para consultar a conta, o sistema deve negar o acesso.

- **FA-003 — Nenhuma transação:**  
  Caso não existam transações registradas, o sistema deve informar que não há movimentações disponíveis.

**Resultado:**  
Histórico das transações da conta apresentado ao cliente.
