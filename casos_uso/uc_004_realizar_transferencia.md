# UC-004 — Realizar Transferência

**Ator principal:**  
Cliente

**Objetivo:**  
Permitir que o cliente transfira valores de sua conta para outra conta válida.

**Pré-condições:**
- O cliente deve estar autenticado.
- A conta de origem deve existir.
- A conta de origem deve estar ativa.
- A conta de destino deve existir.
- O valor deve ser maior que zero.
- A conta de origem deve possuir saldo suficiente.

**Pós-condições:**
- O saldo da conta de origem é reduzido pelo valor transferido.
- O saldo da conta de destino é aumentado pelo mesmo valor.
- A transferência é registrada como uma transação.

**Requisitos relacionados:**  
RF-003, RF-004, RF-005, RF-006

**Regras de negócio relacionadas:**  
RN-002, RN-003, RN-004, RN-005, RN-006

**RNFs relacionados:**  
RNF-001, RNF-002, RNF-003

**Fluxo principal:**

1. Cliente acessa a funcionalidade de transferência.
2. Sistema identifica a conta de origem.
3. Cliente informa a conta de destino.
4. Cliente informa o valor da transferência.
5. Sistema verifica se a conta de origem está ativa.
6. Sistema verifica se a conta de destino é válida.
7. Sistema verifica se o valor é maior que zero.
8. Sistema verifica se a conta de origem possui saldo suficiente.
9. Cliente confirma a transferência.
10. Sistema debita o valor da conta de origem.
11. Sistema credita o valor na conta de destino.
12. Sistema registra a transação.
13. Sistema apresenta a confirmação da transferência.

**Fluxos alternativos/exceções:**

- **FA-001 — Conta de origem inválida:**  
  Caso a conta de origem não exista ou não possa realizar operações, a transferência deve ser rejeitada.

- **FA-002 — Conta de destino inválida:**  
  Caso a conta de destino não exista ou não esteja disponível para receber a operação, a transferência deve ser rejeitada.

- **FA-003 — Valor inválido:**  
  Caso o valor seja igual ou inferior a zero, a transferência deve ser rejeitada.

- **FA-004 — Saldo insuficiente:**  
  Caso o saldo disponível seja inferior ao valor da transferência, a operação deve ser rejeitada.

- **FA-005 — Falha durante a transferência:**  
  Caso ocorra uma falha durante o processamento, o sistema não deve deixar apenas o débito ou apenas o crédito efetivado.

- **FA-006 — Cancelamento:**  
  Caso o cliente não confirme a operação, nenhuma alteração de saldo deve ser realizada.

**Resultado:**  
Valor transferido entre as contas, saldos atualizados e transação registrada.
