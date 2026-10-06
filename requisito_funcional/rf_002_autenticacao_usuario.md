# RF-002 — Autenticação de Usuário

**Título:**  
Autenticação de usuário para acesso ao sistema.

**Descrição:**  
O sistema deve permitir o acesso às funcionalidades e aos dados restritos 
somente após a autenticação do usuário.

**Objetivo:**  
Garantir que apenas usuários autenticados tenham acesso às funcionalidades e 
aos dados protegidos do sistema bancário.

**Stakeholders:**  
Cliente.

**Ator principal:**  
Cliente.

**Pré-condições:**  
- O usuário deve estar cadastrado no sistema.

**Entradas:**  
Credenciais do usuário, como identificador e senha.

**Processamento esperado:**  
O sistema deve validar as credenciais informadas e, quando forem válidas, 
deve autenticar o usuário e iniciar uma sessão de acesso.

**Saídas/Resultados:**  
Sessão autenticada ou mensagem informando que as credenciais são inválidas.

**Pós-condições:**  
O usuário autenticado deve possuir acesso às funcionalidades permitidas 
pelo sistema.

**Fluxos alternativos/exceções:**  
- Caso as credenciais sejam inválidas, o acesso deve ser negado.

**Regras de negócio relacionadas:**  
RN-002

**Prioridade:**  
Crítica

**Status:**  
Aprovado

**Critérios de aceite:**  
- O sistema deve permitir o acesso quando forem fornecidas credenciais válidas.
- O sistema deve impedir o acesso quando forem fornecidas credenciais inválidas.
- O sistema deve criar uma sessão para o usuário após uma autenticação válida.

**Casos de uso relacionados:**  
UC-002

**Tarefas relacionadas:**  
TASK-XXX

**Casos de teste relacionados:**  
CT-XXX
