# UC-001 — Autenticar Usuário

**Ator principal:**
Cliente

**Objetivo:**
Permitir que o cliente acesse as funcionalidades protegidas do sistema após a validação de suas credenciais.

**Pré-condições:**

* O cliente deve estar cadastrado no sistema.
* O cliente deve possuir credenciais de acesso.

**Pós-condições:**

* O cliente estará autenticado.
* Uma sessão de acesso será estabelecida.

**Requisitos relacionados:**
RF-001

**Regras de negócio relacionadas:**
RN-001

**RNFs relacionados:**
RNF-001

**Fluxo principal:**

1. Cliente acessa o sistema.
2. Sistema solicita as credenciais de acesso.
3. Cliente informa suas credenciais.
4. Sistema recebe as credenciais.
5. Sistema valida as credenciais.
6. Sistema autentica o cliente.
7. Sistema estabelece uma sessão.
8. Sistema disponibiliza as funcionalidades permitidas ao cliente.

**Fluxos alternativos/exceções:**

* **FA-001 — Credenciais inválidas:**
  No passo 5, caso as credenciais sejam inválidas, o sistema deve negar o acesso e informar que as credenciais não são válidas.

* **FA-002 — Usuário impedido:**
  No passo 5, caso o usuário esteja impedido de acessar o sistema, o sistema deve negar o acesso.

**Resultado:**
Cliente autenticado e autorizado a acessar as funcionalidades permitidas.
