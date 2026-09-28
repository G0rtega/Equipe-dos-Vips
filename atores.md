# Identificação dos Atores — Sistema Bancário

## Modelo

A identificação de cada ator segue o seguinte modelo:

> **Ator → possui um objetivo → interage com → Sistema → produz um resultado**

Após identificar a interação principal, ela pode ser detalhada por meio de um
**Caso de Uso textual**, que descreve passo a passo como a interação acontece.

### Estrutura

**Ator → Objetivo → Interação → Sistema → Resultado**

Depois:

**Caso de Uso → Passo a passo da interação entre Ator e Sistema**

---

# Atores Identificados

## ATOR-001 — Cliente

**Ator:**
Cliente

**Objetivo:**
Acessar sua conta e realizar operações bancárias permitidas pelo sistema.

**Principais interações:**

* Autenticar-se no sistema.
* Consultar saldo.
* Realizar saque.
* Realizar transferência.
* Consultar histórico de transações.

**Resultado esperado:**
A operação solicitada é validada e, quando permitida, processada pelo sistema,
com o resultado apresentado ao cliente.

**Fluxo resumido:**

> **Cliente → Realizar operação bancária → Sistema Bancário → Operação processada e resultado apresentado**

### Exemplo de Caso de Uso

**UC-001 — Autenticar Usuário**

**Ator:**
Cliente

**Passo a passo:**

1. Cliente acessa o sistema.
2. Sistema solicita as credenciais de acesso.
3. Cliente informa suas credenciais.
4. Sistema valida as credenciais.
5. Sistema autentica o cliente quando as credenciais forem válidas.
6. Sistema disponibiliza as funcionalidades permitidas ao cliente.

**Resultado:**
Cliente autenticado e autorizado a acessar as funcionalidades permitidas.

---

## ATOR-002 — Operador de Suporte

**Ator:**
Operador de Suporte

**Objetivo:**
Consultar informações necessárias para auxiliar clientes e analisar operações
bancárias.

**Principais interações:**

* Consultar informações de contas.
* Consultar transações.
* Consultar detalhes de uma transação.
* Consultar o histórico de movimentações.

**Resultado esperado:**
O operador obtém as informações necessárias para analisar uma operação e
auxiliar no atendimento ao cliente.

**Fluxo resumido:**

> **Operador de Suporte → Consultar informações → Sistema Bancário → Informações apresentadas**

### Exemplo de Caso de Uso

**UC-002 — Consultar Transação para Suporte**

**Ator:**
Operador de Suporte

**Passo a passo:**

1. Operador de Suporte inicia uma consulta.
2. Sistema solicita os dados necessários para localizar a transação.
3. Operador informa os dados da consulta.
4. Sistema localiza as transações correspondentes.
5. Sistema apresenta as transações encontradas.
6. Operador seleciona uma transação.
7. Sistema apresenta os detalhes da transação.

**Resultado:**
As informações da transação ficam disponíveis para análise e atendimento.

---

## ATOR-003 — Administrador Operacional

**Ator:**
Administrador Operacional

**Objetivo:**
Administrar e monitorar informações operacionais do sistema bancário.

**Principais interações:**

* Consultar contas.
* Consultar transações.
* Consultar histórico de operações.
* Monitorar a situação das operações.
* Consultar informações necessárias para manutenção do sistema.

**Resultado esperado:**
O administrador obtém uma visão operacional das informações disponíveis no
sistema.

**Fluxo resumido:**

> **Administrador Operacional → Consultar informações operacionais → Sistema Bancário → Informações apresentadas**

### Exemplo de Caso de Uso

**UC-003 — Consultar Informações Operacionais**

**Ator:**
Administrador Operacional

**Passo a passo:**

1. Administrador Operacional acessa a área administrativa.
2. Sistema verifica a autenticação e as permissões do administrador.
3. Administrador seleciona o tipo de informação que deseja consultar.
4. Sistema recupera as informações solicitadas.
5. Sistema apresenta os dados ao administrador.

**Resultado:**
As informações operacionais solicitadas ficam disponíveis para consulta.

---

# Resumo dos Atores

| ID       | Ator                      | Objetivo principal                 | Principais interações                                                | Resultado principal                  |
| -------- | ------------------------- | ---------------------------------- | -------------------------------------------------------------------- | ------------------------------------ |
| ATOR-001 | Cliente                   | Realizar operações bancárias       | Autenticar, consultar saldo, sacar, transferir e consultar histórico | Operação processada                  |
| ATOR-002 | Operador de Suporte       | Auxiliar no atendimento            | Consultar contas e transações                                        | Informações disponíveis para suporte |
| ATOR-003 | Administrador Operacional | Monitorar informações operacionais | Consultar contas, transações e operações                             | Informações operacionais disponíveis |

---

# Relação entre Atores, Objetivos e Casos de Uso

A partir dos atores identificados, podemos derivar os casos de uso.

| Ator                      | Objetivo                           | Caso de Uso                                 |
| ------------------------- | ---------------------------------- | ------------------------------------------- |
| Cliente                   | Autenticar-se                      | UC-001 — Autenticar Usuário                 |
| Operador de Suporte       | Consultar transação                | UC-002 — Consultar Transação para Suporte   |
| Administrador Operacional | Consultar informações operacionais | UC-003 — Consultar Informações Operacionais |

Outros casos de uso poderão ser derivados posteriormente a partir das
funcionalidades do sistema, como:

* UC-004 — Consultar Saldo
* UC-005 — Realizar Saque
* UC-006 — Realizar Transferência
* UC-007 — Consultar Histórico de Transações

---

# Relação com os Requisitos Funcionais

Os atores e casos de uso devem permanecer alinhados aos requisitos funcionais
do sistema.

| Requisito | Funcionalidade                      | Ator principal |
| --------- | ----------------------------------- | -------------- |
| RF-001    | Autenticação de Usuário             | Cliente        |
| RF-002    | Realização de Saque                 | Cliente        |
| RF-003    | Registro de Transações              | Sistema        |
| RF-004    | Validação do Valor da Operação      | Cliente        |
| RF-005    | Realização de Transferência         | Cliente        |
| RF-006    | Verificação da Situação da Conta    | Sistema        |
| RF-007    | Consulta do Histórico de Transações | Cliente        |

Os requisitos RF-003 e RF-006 representam comportamentos realizados
internamente pelo sistema durante outras operações. Por isso, não é necessário
criar um ator humano específico para cada um deles.

---

# Como identificar um Caso de Uso

Para cada interação identificada, devemos perguntar:

1. **Quem realiza a ação?** → Ator
2. **O que ele deseja fazer?** → Objetivo
3. **O que ele faz no sistema?** → Interação
4. **Como o sistema responde?** → Comportamento do sistema
5. **Qual resultado é produzido?** → Resultado esperado

### Exemplo

> **Cliente → Realizar transferência → Sistema Bancário → Transferência processada**

Pode ser detalhado como:

**UC-006 — Realizar Transferência**

**Ator:**
Cliente

1. Cliente inicia uma nova transferência.
2. Sistema solicita a conta de destino.
3. Cliente informa a conta de destino.
4. Sistema solicita o valor da transferência.
5. Cliente informa o valor.
6. Sistema valida o valor, as contas e o saldo disponível.
7. Cliente confirma a operação.
8. Sistema realiza o débito da conta de origem.
9. Sistema realiza o crédito na conta de destino.
10. Sistema registra a transação.
11. Sistema apresenta o resultado da transferência.

**Resultado:**
Transferência realizada e registrada no sistema.

---

# Observação

Um mesmo ator pode possuir **vários objetivos** e, consequentemente, participar
de vários casos de uso.

No sistema bancário, por exemplo:

> **Cliente**
>
> → Autenticar-se
> → Consultar saldo
> → Realizar saque
> → Realizar transferência
> → Consultar histórico

Cada objetivo pode representar um **Caso de Uso diferente**, desde que
represente uma interação relevante entre o ator e o sistema.

O sistema será posteriormente implementado como uma API simples utilizando
**Supabase**, com o objetivo de simular as operações básicas de um sistema
bancário. As funcionalidades e regras que dependam de recursos ainda não
definidos devem ser especificadas antes de sua implementação.
