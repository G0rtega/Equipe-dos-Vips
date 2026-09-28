# UC-002 — Consultar Saldo

**Ator principal:**  
Cliente

**Objetivo:**  
Permitir que o cliente consulte o saldo disponível de sua conta.

**Pré-condições:**
- O cliente deve estar autenticado.
- O cliente deve possuir uma conta cadastrada.

**Pós-condições:**
- O saldo da conta permanece inalterado.
- O saldo disponível é apresentado ao cliente.

**Requisitos relacionados:**  
RF-XXX — Consulta de Saldo

**Regras de negócio relacionadas:**  
RN-001

**RNFs relacionados:**  
RNF-001, RNF-002

**Fluxo principal:**

1. Cliente acessa a funcionalidade de consulta de saldo.
2. Sistema identifica o cliente autenticado.
3. Sistema identifica a conta associada ao cliente.
4. Sistema consulta o saldo disponível.
5. Sistema apresenta o saldo ao cliente.

**Fluxos alternativos/exceções:**

- **FA-001 — Cliente não autenticado:**  
  Caso o cliente não esteja autenticado, o sistema deve impedir a consulta.

- **FA-002 — Conta inexistente:**  
  Caso não exista uma conta associada ao cliente, o sistema deve informar que não há conta disponível para consulta.

**Resultado:**  
Saldo disponível da conta apresentado ao cliente.
