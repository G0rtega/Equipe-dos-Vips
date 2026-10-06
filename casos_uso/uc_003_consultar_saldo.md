# UC-003 — Consultar Saldo

**Ator principal:**  
Cliente.

**Objetivo:**  
Permitir que o cliente consulte o saldo disponível de sua conta.

**Pré-condições:**
- O cliente deve estar autenticado.
- O cliente deve possuir uma conta cadastrada.

**Pós-condições:**
- O saldo da conta permanece inalterado.
- O saldo disponível é apresentado ao cliente.

**Requisitos relacionados:**  
RF-008 — Consulta de Saldo

**Regras de negócio relacionadas:**  
RN-002

**RNFs relacionados:**  
RNF-001

**Fluxo principal:**

1. O cliente acessa a funcionalidade de consulta de saldo.
2. O sistema identifica o cliente autenticado.
3. O sistema identifica a conta associada ao cliente.
4. O sistema consulta o saldo disponível.
5. O sistema apresenta o saldo ao cliente.

**Fluxos alternativos/exceções:**

- **FA-001 — Cliente não autenticado:**  
  Caso o cliente não esteja autenticado, o sistema deve impedir a consulta.

- **FA-002 — Conta inexistente:**  
  Caso não exista uma conta associada ao cliente, o sistema deve informar que 
  não há conta disponível para consulta.

**Resultado:**  
Saldo disponível da conta apresentado ao cliente.

**Rastreabilidade:**  
RN-002 → RF-008 → UC-003 → CT-XXX
