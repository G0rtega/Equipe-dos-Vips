# RN-002 — Autenticação Obrigatória

**Título:**  
Autenticação obrigatória para acesso ao sistema.

**Descrição:**  
O acesso às funcionalidades e dados restritos do sistema bancário deve ser 
realizado somente por usuários autenticados.

**Origem:**  
Processo de autenticação e segurança do sistema.

**Stakeholders envolvidos:**  
Cliente pagador e operador de suporte.

**Condição:**  
Quando um usuário tentar acessar dados ou funcionalidades restritas do sistema.

**Regra:**  
O sistema deve verificar a autenticação e a sessão do usuário antes de permitir 
o acesso a dados ou operações protegidas.

**Exceções:**  
Funcionalidades que não exigem autenticação, caso sejam disponibilizadas pelo 
sistema.

**Dados envolvidos:**  
Usuário, credenciais e sessão de autenticação.

**Prioridade:**  
Crítica

**Status:**  
Aprovado

**Requisitos relacionados:**  
RF-002

**Observações:**  
A autenticação será realizada por meio do mecanismo de autenticação definido 
para o sistema, como o Supabase Auth.
