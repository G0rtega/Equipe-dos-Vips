# UC-007 — Consultar Informações Operacionais

**Ator principal:**  
Administrador Operacional

**Objetivo:**  
Permitir que o administrador consulte informações operacionais do sistema.

**Pré-condições:**
- O administrador deve estar autenticado.
- O administrador deve possuir as permissões necessárias.

**Pós-condições:**
- As informações solicitadas são apresentadas ao administrador.
- Nenhuma operação financeira é alterada pela consulta.

**Requisitos relacionados:**  
RF-003, RF-006

**Regras de negócio relacionadas:**  
RN-001, RN-003, RN-006

**RNFs relacionados:**  
RNF-001, RNF-002, RNF-006

**Fluxo principal:**

1. Administrador Operacional acessa a área administrativa.
2. Sistema verifica a autenticação e as permissões do administrador.
3. Administrador seleciona o tipo de informação que deseja consultar.
4. Sistema recupera as informações solicitadas.
5. Sistema apresenta os dados ao administrador.
6. Administrador analisa as informações apresentadas.

**Fluxos alternativos/exceções:**

- **FA-001 — Administrador não autenticado:**  
  Caso o administrador não esteja autenticado, o sistema deve impedir o acesso.

- **FA-002 — Sem permissão:**  
  Caso o administrador não possua a permissão necessária, o sistema deve negar o acesso.

- **FA-003 — Dados não encontrados:**  
  Caso não existam informações correspondentes à consulta, o sistema deve informar que nenhum dado foi encontrado.

**Resultado:**  
Informações operacionais disponibilizadas para consulta administrativa.
