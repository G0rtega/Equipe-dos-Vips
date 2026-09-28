# UC-006 — Consultar Transação para Suporte

**Ator principal:**  
Operador de Suporte

**Objetivo:**  
Permitir que o operador consulte informações de uma transação para auxiliar no atendimento ao cliente.

**Pré-condições:**
- O operador deve estar autenticado.
- O operador deve possuir permissão para realizar consultas de suporte.

**Pós-condições:**
- As informações da transação são apresentadas ao operador.
- Nenhuma informação financeira é alterada pela consulta.

**Requisitos relacionados:**  
RF-003, RF-007

**Regras de negócio relacionadas:**  
RN-001, RN-003, RN-007

**RNFs relacionados:**  
RNF-001, RNF-002

**Fluxo principal:**

1. Operador de Suporte acessa a funcionalidade de consulta.
2. Sistema verifica a autenticação e a permissão do operador.
3. Sistema solicita os dados necessários para localizar a transação.
4. Operador informa os dados da consulta.
5. Sistema localiza as transações correspondentes.
6. Sistema apresenta as transações encontradas.
7. Operador seleciona uma transação.
8. Sistema apresenta os detalhes da transação.

**Fluxos alternativos/exceções:**

- **FA-001 — Operador não autenticado:**  
  Caso o operador não esteja autenticado, o sistema deve impedir a consulta.

- **FA-002 — Sem permissão:**  
  Caso o operador não possua permissão de suporte, o sistema deve negar o acesso.

- **FA-003 — Transação não encontrada:**  
  Caso nenhuma transação corresponda aos dados informados, o sistema deve informar que nenhuma transação foi encontrada.

**Resultado:**  
Informações da transação disponibilizadas para análise do operador.
