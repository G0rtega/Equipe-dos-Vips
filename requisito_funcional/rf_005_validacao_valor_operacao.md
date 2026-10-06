# RF-005 — Validação do Valor da Operação

**Título:**  
Validação do valor das operações financeiras.

**Descrição:**  
O sistema deve validar se o valor informado para uma operação financeira é 
maior que zero antes de permitir sua efetivação.

**Objetivo:**  
Impedir operações financeiras com valores inválidos e evitar alterações 
incorretas nos saldos das contas.

**Stakeholders:**  
Cliente.

**Ator principal:**  
Sistema.

**Pré-condições:**  
- Uma operação financeira deve ter sido solicitada.

**Entradas:**  
Valor da operação.

**Processamento esperado:**  
O sistema deve verificar se o valor informado é maior que zero antes de 
permitir a continuidade da operação.

**Saídas/Resultados:**  
Operação aprovada para processamento ou mensagem indicando que o valor é 
inválido.

**Pós-condições:**  
Valores válidos podem prosseguir para processamento. Valores inválidos não 
devem alterar os dados financeiros do sistema.

**Fluxos alternativos/exceções:**  
Caso o valor seja igual ou inferior a zero, a operação deve ser rejeitada.

**Regras de negócio relacionadas:**  
RN-005

**Prioridade:**  
Alta

**Status:**  
Aprovado

**Critérios de aceite:**  
- O sistema deve aceitar valores maiores que zero.
- O sistema deve rejeitar valores iguais a zero.
- O sistema deve rejeitar valores inferiores a zero.
- Uma operação com valor inválido não deve alterar o saldo da conta.

**Casos de uso relacionados:**  
UC-004, UC-005

**Tarefas relacionadas:**  
TASK-XXX

**Casos de teste relacionados:**  
CT-XXX
