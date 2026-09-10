# RF-001 — Autenticar Usuário

**Título:**  
Autenticar usuário no sistema.

**Descrição:**  
O sistema deve permitir que usuários cadastrados realizem autenticação para 
acessar as funcionalidades e os dados restritos do sistema bancário.

**Objetivo:**  
Garantir que somente usuários autenticados tenham acesso às informações e 
operações protegidas do sistema.

**Stakeholders:**  
Cliente pagador, cliente recebedor, operador de suporte e administrador 
operacional.

**Ator principal:**  
Usuário.

**Pré-condições:**  
- Usuário deve estar cadastrado no sistema.
- Usuário deve possuir credenciais de acesso.

**Entradas:**  
- E-mail, identificador do usuário ou número da conta.
- Senha ou outra credencial de autenticação.

**Processamento esperado:**  
O sistema deve validar as credenciais informadas pelo usuário. Caso sejam 
válidas, o sistema deve autenticar o usuário e estabelecer uma sessão de acesso.

**Saídas/Resultados:**  
Usuário autenticado e sessão de acesso estabelecida.

**Pós-condições:**  
O usuário poderá acessar as funcionalidades permitidas para seu perfil enquanto 
sua sessão estiver válida.

**Fluxos alternativos/exceções:**  
- Credenciais inválidas: o sistema deve negar o acesso e informar que a 
autenticação não foi realizada.
- Usuário não cadastrado: o sistema deve negar o acesso.
- Usuário desabilitado: o sistema deve negar o acesso.
- Sessão expirada ou inválida: o sistema deve exigir uma nova autenticação.

**Regras de negócio relacionadas:**  
RN-001

**Prioridade:**  
Crítica

**Status:**  
Proposto

**Critérios de aceite:**  
- Permitir acesso somente quando as credenciais forem válidas.
- Negar acesso quando as credenciais forem inválidas.
- Estabelecer uma sessão após uma autenticação bem-sucedida.
- Permitir acesso somente às funcionalidades autorizadas para o perfil do 
usuário.
- Exigir nova autenticação quando a sessão estiver expirada ou inválida.

**Casos de uso relacionados:**  
UC-001

**Tarefas relacionadas:**  
TASK-001

**Casos de teste relacionados:**  
CT-001, CT-002, CT-003
