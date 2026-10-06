## RNF-001 — Segurança de Autenticação

**Categoria:**  
Segurança

**Descrição:**  
O sistema deve proteger as credenciais dos usuários e impedir o acesso às 
funcionalidades protegidas por usuários não autenticados.

**Justificativa:**  
Garantir a proteção dos dados bancários e impedir acessos não autorizados às 
contas e operações do sistema.

**Métrica/Critério mensurável:**  
100% das funcionalidades classificadas como protegidas devem exigir uma sessão 
de usuário autenticada. Senhas não devem ser armazenadas em texto simples.

**Escopo:**  
Todo o sistema, especialmente as funcionalidades que envolvem dados pessoais 
e financeiros.

**Prioridade:**  
Crítica

**Status:**  
Aprovado

**Requisitos relacionados:**  
RF-002, RF-003, RF-006, RF-007

**Casos de teste relacionados:**  
CT-XXX
