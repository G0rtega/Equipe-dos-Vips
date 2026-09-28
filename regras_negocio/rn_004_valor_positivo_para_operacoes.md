# RN-004 — Valor Positivo para Operações

**Título:**  
Operações financeiras devem possuir valor positivo.

**Descrição:**  
Operações financeiras que envolvam movimentação de valores devem possuir um 
valor maior que zero.

**Origem:**  
Processo de validação das operações financeiras do sistema.

**Stakeholders envolvidos:**  
Cliente pagador, cliente recebedor, operador de suporte e administrador 
operacional.

**Condição:**  
Quando um usuário autorizado solicitar uma operação financeira que envolva 
movimentação de valores.

**Regra:**  
O sistema deve verificar se o valor informado é maior que zero antes de 
efetivar a operação. Operações com valor igual ou inferior a zero não devem 
ser realizadas.

**Exceções:**  
Não se aplica a operações que não envolvam movimentação financeira.

**Dados envolvidos:**  
Valor da operação, tipo da operação e conta envolvida.

**Prioridade:**  
Alta

**Status:**  
Aprovado

**Requisitos relacionados:**  
RF-004

**Observações:**  
A validação deve ocorrer antes de qualquer alteração no saldo das contas.
