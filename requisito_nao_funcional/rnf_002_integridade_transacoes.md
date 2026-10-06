## RNF-002 — Integridade das Transações

**Categoria:**  
Integridade

**Descrição:**  
O sistema deve garantir que as transações financeiras sejam realizadas de forma 
consistente, evitando alterações parciais ou incorretas nos dados das contas.

**Justificativa:**  
Garantir que os valores financeiros das contas permaneçam consistentes após a 
realização de operações como saques e transferências.

**Métrica/Critério mensurável:**  
100% das transferências realizadas devem resultar no débito do valor na conta 
de origem e no crédito do mesmo valor na conta de destino. Em caso de falha, 
nenhuma alteração parcial deve ser mantida.

**Escopo:**  
Operações financeiras que alteram o saldo das contas, especialmente saques e 
transferências.

**Prioridade:**  
Crítica

**Status:**  
Aprovado

**Requisitos relacionados:**  
RF-003, RF-004, RF-006

**Casos de teste relacionados:**  
CT-XXX
