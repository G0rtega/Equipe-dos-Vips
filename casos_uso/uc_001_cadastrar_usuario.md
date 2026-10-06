# UC-001 — Cadastrar Usuário

**Ator principal:**  
Cliente.

**Objetivo:**  
Permitir que uma pessoa realize seu cadastro no sistema para posteriormente 
acessar as funcionalidades disponíveis.

**Pré-condições:**
- O usuário ainda não deve possuir cadastro no sistema.

**Pós-condições:**
- O usuário deve estar cadastrado no sistema.
- As informações do usuário devem estar armazenadas para permitir sua 
  autenticação posteriormente.

**Requisitos relacionados:**  
RF-001

**Regras de negócio relacionadas:**  
RN-001

**RNFs relacionados:**  
RNF-001

**Fluxo principal:**

1. O cliente solicita o cadastro de um novo usuário.
2. O sistema apresenta os dados necessários para o cadastro.
3. O cliente informa os dados solicitados.
4. O sistema recebe os dados informados.
5. O sistema valida os dados obrigatórios.
6. O sistema verifica se o identificador do usuário já está cadastrado.
7. O sistema cria o cadastro do usuário.
8. O sistema informa que o cadastro foi realizado com sucesso.

**Fluxos alternativos/exceções:**

- **FA-001 — Dados obrigatórios ausentes:**  
  Caso algum dado obrigatório não seja informado, o sistema deve rejeitar o 
  cadastro e informar os campos que precisam ser preenchidos.

- **FA-002 — Dados inválidos:**  
  Caso algum dado informado seja inválido, o sistema deve rejeitar o cadastro 
  e informar o erro correspondente.

- **FA-003 — Usuário já cadastrado:**  
  Caso o identificador informado já esteja associado a outro usuário, o 
  sistema deve impedir a criação de um cadastro duplicado.

**Resultado:**  
Usuário cadastrado com sucesso e apto a realizar a autenticação no sistema.

**Rastreabilidade** 
RN-001 → RF-001 → UC-001 → CT-XXX
