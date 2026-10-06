# UC-005 — Realizar Transferência

**Ator principal:**  
Cliente.

**Objetivo:**  
Permitir que o cliente transfira valores de sua conta para outra conta válida.

**Pré-condições:**
- O cliente deve estar autenticado.
- A conta de origem deve existir no sistema.
- A conta de destino deve existir no sistema.

**Pós-condições:**
- O saldo da conta de origem é reduzido pelo valor transferido.
- O saldo da conta de destino é aumentado pelo mesmo valor.
- A transferência é registrada como uma transação.

**Requisitos relacionados:**  
RF-004, RF-005, RF-006

**Regras de negócio relacionadas:**  
RN-004, RN-005, RN-006

**RNFs relacionados:**  
RNF-001, RNF-002

**Fluxo principal:**

1. O cliente acessa a funcionalidade de transferência.
2. O sistema identifica a conta de origem.
3. O cliente informa a conta de destino.
4. O cliente informa o valor da transferência.
5. O sistema verifica se a conta de destino é válida.
6. O sistema verifica se o valor é maior que zero.
7. O sistema verifica se a conta de origem possui saldo suficiente.
8. O cliente confirma a transferência.
9. O sistema debita o valor da conta de origem.
10. O sistema credita o mesmo valor na conta de destino.
11. O sistema registra a transação.
12. O sistema apresenta a confirmação da transferência.

**Fluxos alternativos/exceções:**

- **FA-001 — Conta de destino inválida:**  
  No passo 5, caso a conta de destino não exista, a transferência deve ser 
  rejeitada.

- **FA-002 — Valor inválido:**  
  No passo 6, caso o valor seja igual ou inferior a zero, a transferência deve 
  ser rejeitada.

- **FA-003 — Saldo insuficiente:**  
  No passo 7, caso o saldo disponível seja inferior ao valor da transferência, 
  a operação deve ser rejeitada.

- **FA-004 — Falha durante a transferência:**  
  Caso ocorra uma falha durante o processamento, o sistema não deve deixar 
  apenas o débito ou apenas o crédito efetivado.

- **FA-005 — Cancelamento:**  
  Caso o cliente não confirme a operação, nenhuma alteração de saldo deve ser 
  realizada.

**Resultado:**  
Valor transferido entre as contas, saldos atualizados e transação registrada.

**Rastreabilidade:**  
RN-004 → RF-004 → UC-005 → CT-XXX  
RN-005 → RF-005 → UC-005 → CT-XXX  
RN-006 → RF-006 → UC-005 → CT-XXX
