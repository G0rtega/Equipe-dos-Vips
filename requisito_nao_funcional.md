# RNF-001 — Segurança da Autenticação

**Categoria:**  
Segurança

**Descrição:**  
O sistema deve proteger o processo de autenticação e impedir o acesso não 
autorizado às contas e funcionalidades restritas.

**Justificativa:**  
A autenticação envolve o acesso a dados financeiros e operações bancárias, 
sendo necessário impedir acessos não autorizados. Caso contrário clientes serão
afetados negativamente com perda financeira.

**Métrica/Critério mensurável:**  
100% das tentativas de acesso a funcionalidades restritas devem exigir uma 
sessão de autenticação válida.

**Escopo:**  
Todo o sistema, especialmente as funcionalidades que envolvem dados de usuários,
contas e transações.

**Prioridade:**  
Crítica

**Status:**  
Proposto

**Requisitos relacionados:**  
RF-001

**Casos de teste relacionados:**  
CT-001, CT-002
