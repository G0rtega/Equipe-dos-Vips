# UC-004 — Realizar Saque

**Ator principal:**  
Cliente.

**Objetivo:**  
Permitir que o cliente realize um saque de sua conta quando todas as regras 
necessárias forem atendidas.

**Pré-condições:**
- O cliente deve estar autenticado.
- A conta deve existir no sistema.

**Pós-condições:**
- O saldo da conta é reduzido pelo valor do saque.
- A transação é registrada.
- O saque fica disponível no histórico da conta.

**Requisitos relacionados:**  
RF-003, RF-004, RF-005

**Regras de negócio relacionadas:**  
RN-003, RN-004, RN-005

**RNFs relacionados:**  
RNF-001, RNF-002

**Fluxo principal:**

1. O cliente acessa a funcionalidade de saque.
2. O sistema identifica a conta do cliente.
3. O cliente informa o valor do saque.
4. O sistema valida se o valor é maior que zero.
5. O sistema verifica se existe saldo suficiente.
6. O cliente confirma o saque.
7. O sistema desconta o valor do saldo da conta.
8. O sistema registra a transação.
9. O sistema apresenta a confirmação do saque.

**Fluxos alternativos/exceções:**

- **FA-001 — Valor inválido:**  
  No passo 4, caso o valor seja igual ou inferior a zero, o sistema deve 
  rejeitar a operação.

- **FA-002 — Saldo insuficiente:**  
  No passo 5, caso o saldo seja inferior ao valor solicitado, o sistema deve 
  impedir o saque.

- **FA-003 — Cancelamento:**  
  Caso o cliente não confirme a operação, o sistema não deve alterar o saldo 
  nem registrar a operação como concluída.

**Resultado:**  
Saque realizado, saldo atualizado e transação registrada.

**Rastreabilidade:**  
RN-003 → RF-003 → UC-004
RN-004 → RF-004 → UC-004
RN-005 → RF-005 → UC-004
