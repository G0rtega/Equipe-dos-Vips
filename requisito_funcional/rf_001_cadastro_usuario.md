# RF-001 — Cadastro de Usuário

**Título:**  
Cadastro de novo usuário.

**Descrição:**  
O sistema deve permitir o cadastro de um novo usuário mediante o fornecimento 
de dados obrigatórios válidos.

**Objetivo:**  
Permitir que uma pessoa faça um cadastro de usuário para acessar as 
funcionalidades do sistema bancário.

**Stakeholders:**  
Cliente.

**Ator principal:**  
Cliente.

**Pré-condições:**  
- O usuário ainda não deve possuir cadastro no sistema.

**Entradas:**  
Nome, e-mail, credenciais de acesso e demais dados obrigatórios do usuário.

**Processamento esperado:**  
O sistema deve validar os dados informados e verificar se o identificador do 
usuário já está cadastrado. Caso os dados sejam válidos e o usuário ainda não 
exista, o sistema deve criar o cadastro.

**Saídas/Resultados:**  
Usuário cadastrado com sucesso.

**Pós-condições:**  
- O usuário deve estar registrado no sistema.
- O usuário poderá realizar a autenticação para acessar as funcionalidades 
  disponíveis.

**Fluxos alternativos/exceções:**  
- Dados obrigatórios ausentes: o sistema deve informar os campos que precisam 
  ser preenchidos.
- Dados inválidos: o sistema deve rejeitar o cadastro e informar o erro.
- Usuário já cadastrado: o sistema deve impedir a criação de um cadastro 
  duplicado.

**Regras de negócio relacionadas:**  
RN-001

**Prioridade:**  
Alta

**Status:**  
Aprovado

**Critérios de aceite:**  
- O sistema deve permitir o cadastro quando todos os dados obrigatórios forem 
  válidos.
- O sistema não deve permitir cadastro com dados obrigatórios ausentes ou 
  inválidos.
- O sistema não deve permitir identificadores duplicados.
- Após o cadastro, o usuário deve poder realizar a autenticação.

**Casos de uso relacionados:**  
UC-001

**Tarefas relacionadas:**  
TASK-XXX

**Casos de teste relacionados:**  
CT-XXX
