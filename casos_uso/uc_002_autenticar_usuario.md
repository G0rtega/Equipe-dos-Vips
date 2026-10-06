# UC-002 — Autenticar Usuário

**Ator principal:**  
Cliente.

**Objetivo:**  
Permitir que o cliente acesse as funcionalidades protegidas do sistema após a 
validação de suas credenciais.

**Pré-condições:**
- O cliente deve estar cadastrado no sistema.
- O cliente deve possuir credenciais de acesso.

**Pós-condições:**
- O cliente estará autenticado.
- Uma sessão de acesso será estabelecida.

**Requisitos relacionados:**  
RF-002

**Regras de negócio relacionadas:**  
RN-002

**RNFs relacionados:**  
RNF-001

**Fluxo principal:**

1. O cliente acessa o sistema.
2. O sistema solicita as credenciais de acesso.
3. O cliente informa suas credenciais.
4. O sistema recebe as credenciais.
5. O sistema valida as credenciais.
6. O sistema autentica o cliente.
7. O sistema estabelece uma sessão.
8. O sistema disponibiliza as funcionalidades permitidas ao cliente.

**Fluxos alternativos/exceções:**

- **FA-001 — Credenciais inválidas:**  
  No passo 5, caso as credenciais sejam inválidas, o sistema deve negar o 
  acesso e informar que as credenciais não são válidas.

**Resultado:**  
Cliente autenticado e autorizado a acessar as funcionalidades permitidas.

**Rastreabilidade:**  
RN-002 → RF-002 → UC-002 → CT-XXX
