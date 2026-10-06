# Atores Identificados

## ATOR-001 — Cliente

**Ator:**
Cliente

**Objetivo:**
Acessar sua conta e realizar operações bancárias permitidas pelo sistema.

**Principais interações:**

* Cadastrar-se no sistema.
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

**UC-001 — Cadastrar Usuário**

**Ator:**
Cliente

**Passo a passo:**

1. Cliente solicita o cadastro de um novo usuário.
2. Sistema apresenta os dados necessários para o cadastro.
3. Cliente informa os dados solicitados.
4. Sistema recebe e valida os dados.
5. Sistema verifica se o identificador já está cadastrado.
6. Sistema cria o cadastro do usuário.
7. Sistema informa que o cadastro foi realizado com sucesso.

**Resultado:**
Usuário cadastrado com sucesso e apto a realizar a autenticação no sistema.

---

## ATOR-002 — Operador de Suporte

**Ator:**
Operador de Suporte

**Objetivo:**
Consultar informações necessárias para auxiliar clientes e analisar operações
bancárias.

**Principais interações:**

* Consultar transações.
* Consultar detalhes de uma transação.
* Consultar informações necessárias para o atendimento.

**Resultado esperado:**
O operador obtém as informações necessárias para analisar uma operação e
auxiliar no atendimento ao cliente.

**Fluxo resumido:**

> **Operador de Suporte → Consultar informações → Sistema Bancário → Informações apresentadas**

### Exemplo de Caso de Uso

**UC-007 — Consultar Transação para Suporte**

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

# Resumo dos Atores

| ID       | Ator                | Objetivo principal        | Principais interações                                                   | Resultado principal                  |
| -------- | ------------------- | ------------------------- | ----------------------------------------------------------------------- | ------------------------------------ |
| ATOR-001 | Cliente             | Realizar operações bancárias | Cadastrar, autenticar, consultar saldo, sacar, transferir e consultar histórico | Operação processada                  |
| ATOR-002 | Operador de Suporte | Auxiliar no atendimento   | Consultar transações e informações para suporte                         | Informações disponíveis para suporte |

---

# Relação entre Atores, Objetivos e Casos de Uso

A partir dos atores identificados, podemos relacionar os casos de uso.

| Ator                | Objetivo                           | Caso de Uso                               |
| ------------------- | ---------------------------------- | ----------------------------------------- |
| Cliente             | Cadastrar-se                       | UC-001 — Cadastrar Usuário                |
| Cliente             | Autenticar-se                      | UC-002 — Autenticar Usuário               |
| Cliente             | Consultar saldo                    | UC-003 — Consultar Saldo                  |
| Cliente             | Realizar saque                     | UC-004 — Realizar Saque                   |
| Cliente             | Realizar transferência             | UC-005 — Realizar Transferência           |
| Cliente             | Consultar histórico                | UC-006 — Consultar Histórico de Transações |
| Operador de Suporte | Consultar transação para suporte   | UC-007 — Consultar Transação para Suporte |

---

# Relação com os Requisitos Funcionais

Os atores e casos de uso devem permanecer alinhados aos requisitos funcionais
do sistema.

| Requisito | Funcionalidade                      | Ator principal |
| --------- | ----------------------------------- | -------------- |
| RF-001    | Cadastro de Usuário                 | Cliente        |
| RF-002    | Autenticação de Usuário             | Cliente        |
| RF-003    | Realização de Saque                 | Cliente        |
| RF-004    | Registro de Transações              | Sistema        |
| RF-005    | Validação do Valor da Operação      | Sistema        |
| RF-006    | Realização de Transferência         | Cliente        |
| RF-007    | Consulta do Histórico de Transações | Cliente        |

Os requisitos RF-004 e RF-005 representam comportamentos realizados
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

**UC-005 — Realizar Transferência**

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
> → Cadastrar-se
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
