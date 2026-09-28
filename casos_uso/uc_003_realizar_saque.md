# UC-003 — Realizar Saque

**Ator principal:**  
Cliente

**Objetivo:**  
Permitir que o cliente realize um saque de sua conta quando todas as regras necessárias forem atendidas.

**Pré-condições:**
- O cliente deve estar autenticado.
- A conta deve existir.
- A conta deve estar ativa.
- O valor informado deve ser maior que zero.
- A conta deve possuir saldo suficiente.

**Pós-condições:**
- O saldo da conta é reduzido pelo valor do saque.
- A transação é registrada.
- O saque fica disponível no histórico da conta.

**Requisitos relacionados:**  
RF-002, RF-003, RF-004, RF-006

**Regras de negócio relacionadas:**  
RN-002, RN-003, RN-004, RN-006

**RNFs relacionados:**  
RNF-001, RNF-002, RNF-003

**Fluxo principal:**

1. Cliente acessa a funcionalidade de saque.
2. Sistema identifica a conta do cliente.
3. Sistema verifica se a conta está ativa.
4. Cliente informa o valor do saque.
5. Sistema valida se o valor é maior que zero.
6. Sistema verifica se existe saldo suficiente.
7. Cliente confirma o saque.
8. Sistema desconta o valor do saldo da conta.
9. Sistema registra a transação.
10. Sistema apresenta a confirmação do saque.

**Fluxos alternativos/exceções:**

- **FA-001 — Conta inativa:**  
  No passo 3, caso a conta esteja inativa, bloqueada ou encerrada, o sistema deve impedir o saque.

- **FA-002 — Valor inválido:**  
  No passo 5, caso o valor seja igual ou inferior a zero, o sistema deve rejeitar a operação.

- **FA-003 — Saldo insuficiente:**  
  No passo 6, caso o saldo seja inferior ao valor solicitado, o sistema deve impedir o saque.

- **FA-004 — Cancelamento:**  
  Caso o cliente não confirme a operação, o sistema não deve alterar o saldo nem registrar a operação como concluída.

**Resultado:**  
Saque realizado, saldo atualizado e transação registrada.
