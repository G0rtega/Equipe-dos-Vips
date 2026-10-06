# UC-007 — Consultar Transação para Suporte

**Ator principal:**  
Operador de Suporte.

**Objetivo:**  
Permitir que o operador consulte informações de uma transação para auxiliar 
no atendimento ao cliente.

**Pré-condições:**
- O operador deve estar autenticado.
- O operador deve possuir permissão para realizar consultas de suporte.

**Pós-condições:**
- As informações da transação são apresentadas ao operador.
- Nenhuma informação financeira é alterada pela consulta.

**Requisitos relacionados:**  
RF-004, RF-007

**Regras de negócio relacionadas:**  
RN-002, RN-004, RN-007

**RNFs relacionados:**  
RNF-001, RNF-002

**Fluxo principal:**

1. O operador de suporte acessa a funcionalidade de consulta.
2. O sistema verifica a autenticação e a permissão do operador.
3. O sistema solicita os dados necessários para localizar a transação.
4. O operador informa os dados da consulta.
5. O sistema localiza as transações correspondentes.
6. O sistema apresenta as transações encontradas.
7. O operador seleciona uma transação.
8. O sistema apresenta os detalhes da transação.

**Fluxos alternativos/exceções:**

- **FA-001 — Operador não autenticado:**  
  Caso o operador não esteja autenticado, o sistema deve impedir a consulta.

- **FA-002 — Sem permissão:**  
  Caso o operador não possua permissão de suporte, o sistema deve negar o 
  acesso.

- **FA-003 — Transação não encontrada:**  
  Caso nenhuma transação corresponda aos dados informados, o sistema deve 
  informar que nenhuma transação foi encontrada.

**Resultado:**  
Informações da transação disponibilizadas para análise do operador.

**Rastreabilidade:**  
RN-002 → RF-007 → UC-007 → CT-XXX  
RN-004 → RF-004 → UC-007 → CT-XXX  
RN-007 → RF-007 → UC-007 → CT-XXX
