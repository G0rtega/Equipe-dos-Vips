# RN-003 — Registro de Transações Bancárias

**Título:**  
Registro obrigatório das transações realizadas.

**Descrição:**  
Toda operação financeira efetivada pelo sistema deve ser registrada para 
permitir a consulta e o rastreamento das movimentações realizadas.

**Origem:**  
Processo de controle e rastreamento das operações bancárias.

**Stakeholders envolvidos:**  
Cliente pagador, cliente recebedor, operador de suporte e administrador 
operacional.

**Condição:**  
Quando uma operação financeira for efetivada no sistema, como depósito, saque 
ou transferência.

**Regra:**  
O sistema deve registrar cada transação efetivada, armazenando as informações 
necessárias para identificar a operação, seu valor, sua data e as contas 
envolvidas.

**Exceções:**  
Operações que não sejam efetivadas não devem ser registradas como transações 
financeiras concluídas.

**Dados envolvidos:**  
Identificador da transação, tipo da operação, valor, data e hora, conta de 
origem, conta de destino, usuário responsável e status da transação.

**Prioridade:**  
Alta

**Status:**  
Aprovado

**Requisitos relacionados:**  
RF-003

**Observações:**  
O registro das transações deve permitir a consulta do histórico de 
movimentações e auxiliar na identificação de operações realizadas no sistema.
