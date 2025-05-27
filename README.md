
# ✅ Plano de Testes: Fluxo de Login

## 1. Objetivo

Validar as funcionalidades do fluxo de login de usuários, garantindo que todos os campos obrigatórios e as validações funcionem conforme o esperado.

## 2. Escopo

- Login
- Validação de campos obrigatórios

## 3. Critérios de Entrada

- Aplicação disponível.
- Credenciais de teste criadas.

## 4. Critérios de Saída

- Todos os casos executados.
- Bugs identificados e reportados.

## 5. Ambiente

- **Navegador:** Chrome  
- **Sistema Operacional:** macOS

## 6. Responsável

Valter Goes

## 7. Cronograma

- **Início:** 28/05  
- **Fim:** 28/05

---

# 🎯 Cenário de Teste: Fazer Login com Sucesso

**Descrição:**  
Acessar o site preenchendo o formulário de login com usuário e senha válidos, efetuando o login com sucesso.

**Objetivo:**  
Validar que os campos de usuário e senha aceitam dados corretos, direcionando o usuário à página inicial.

**Pré-condições:**  
- Usuário está na tela de login.

**Fluxo Principal:**

1. Preencher campo de usuário.
2. Preencher campo de senha.
3. Clicar no botão de login.

**Critérios de Aceitação:**

- Login realizado com sucesso.
- Redirecionamento para a página Home.

---

## ✅ Casos de Teste

## **ID:** CT-login-001 - Login com dados válidos

**Cenário:** Fazer login com dados válidos

**Descrição:**  
Inserir usuário e senha nos respectivos campos e clicar em login.

**Pré-condições:**  
- Estar na página de login.

**Passos para execução:**

1. Acessar a página de login.
2. Inserir um usuário válido.
3. Inserir uma senha válida.
4. Clicar no botão "Login".

**Dados de entrada:**

| Campo   | Valor          |
|---------|----------------|
| Usuário | standard_user  |
| Senha   | secret_sauce   |

**Resultado Esperado:**  
O usuário deve ser direcionado para a página Home.

**Resultado Obtido:**  
Usuário direcionado para página 'Home’ com produtos exibidos.

**Status:** ✅ **Pass**

**Observações:**  
![Screenshot](img/Screenshot%201%202025-05-27%20at%203.13.50%20PM.png)

---

## **ID:** CT-login-002 - Tentativa de login com dados inválidos

**Cenário:** Tentativa de fazer login com dados inválidos

**Descrição:**  
Inserir usuário e senha inválidos nos respectivos campos e clicar em login.

**Pré-condições:**  
- Estar na página de login.

**Passos para execução:**

1. Acessar a página de login.
2. Inserir um usuário inválido.
3. Inserir uma senha inválida.
4. Clicar no botão "Login".

**Dados de entrada:**

| Campo   | Valor   |
|---------|---------|
| Usuário | standard |
| Senha   | secret  |

**Resultado Esperado:**  
Usuário deve receber uma mensagem de erro.

**Resultado Obtido:**  
Mensagem de erro exibida:  
`Epic sadface: Username and password do not match any user in this service`

**Status:** ✅ **Pass**

**Observações:**  
![Screenshot](img/Screenshot%202%202025-05-27%20at%203.28.03%20PM.png)

---

## **ID:** CT-login-003 - Tentativa de login com usuário inválido

**Cenário:** Tentativa de fazer login com usuário inválido e senha correta

**Descrição:**  
Inserir usuário inválido, senha correta e clicar em login.

**Pré-condições:**  
- Estar na página de login.

**Passos para execução:**

1. Acessar a página de login.
2. Inserir um usuário inválido.
3. Inserir uma senha correta.
4. Clicar no botão "Login".

**Dados de entrada:**

| Campo   | Valor         |
|---------|---------------|
| Usuário | standard      |
| Senha   | secret_sauce  |

**Resultado Esperado:**  
Usuário deve receber uma mensagem de erro informando que o usuário está incorreto.

**Resultado Obtido:**  
Mesma mensagem de erro informando que ambos os campos estão incorretos:  
`Epic sadface: Username and password do not match any user in this service`

**Status:** ❌ **Fail**

**Observações:**  
![Screenshot](img/Screenshot%203%202025-05-27%20at%203.34.37%20PM.png)

---

## **ID:** CT-login-004 - Tentativa de login com senha inválida

**Cenário:** Tentativa de fazer login com senha inválida e usuário correto

**Descrição:**  
Inserir senha inválida, usuário correto e clicar em login.

**Pré-condições:**  
- Estar na página de login.

**Passos para execução:**

1. Acessar a página de login.
2. Inserir um usuário válido.
3. Inserir uma senha incorreta.
4. Clicar no botão "Login".

**Dados de entrada:**

| Campo   | Valor         |
|---------|---------------|
| Usuário | standard_user |
| Senha   | secret        |

**Resultado Esperado:**  
Usuário deve receber uma mensagem de erro informando que a senha está incorreta.

**Resultado Obtido:**  
Mesma mensagem de erro exibida informando que ambos os campos estão incorretos:  
`Epic sadface: Username and password do not match any user in this service`

**Status:** ❌ **Fail**

**Observações:**  
![Screenshot](img/Screenshot%204%202025-05-27%20at%203.39.02%20PM.png)

---

## **ID:** CT-login-005 - Tentativa de login com campos vazios

**Cenário:** Tentativa de fazer login com ambos os campos vazios

**Descrição:**  
Não inserir dados de usuário e senha e clicar em login.

**Pré-condições:**  
- Estar na página de login.

**Passos para execução:**

1. Acessar a página de login.
2. Não inserir um usuário.
3. Não inserir uma senha.
4. Clicar no botão "Login".

**Dados de entrada:**

| Campo   | Valor |
|---------|-------|
| Usuário |       |
| Senha   |       |

**Resultado Esperado:**  
Usuário deve receber uma mensagem de erro informando que ambos os campos são obrigatórios.

**Resultado Obtido:**  
Mensagem de erro exibida:  
`Epic sadface: Username is required`

**Status:** ❌ **Fail**

**Observações:**  
![Screenshot](img/Screenshot%205%202025-05-27%20at%203.43.04%20PM.png)

---

## **ID:** CT-login-006 - Tentativa de login com campo senha vazio

**Cenário:** Tentativa de fazer login com usuário válido e campo senha vazio

**Descrição:**  
Inserir dados de usuário válido, não inserir senha e clicar em login.

**Pré-condições:**  
- Estar na página de login.

**Passos para execução:**

1. Acessar a página de login.
2. Inserir um usuário válido.
3. Não inserir uma senha.
4. Clicar no botão "Login".

**Dados de entrada:**

| Campo   | Valor         |
|---------|---------------|
| Usuário | standard_user |
| Senha   |               |

**Resultado Esperado:**  
Usuário deve receber uma mensagem de erro.

**Resultado Obtido:**  
Mensagem de erro exibida:  
`Epic sadface: Password is required`

**Status:** ✅ **Pass**

**Observações:**  
![Screenshot](img/Screenshot%206%202025-05-27%20at%203.48.33%20PM.png)

---

## **ID:** CT-login-007 - Tentativa de login com campo usuário vazio

**Cenário:** Tentativa de fazer login com campo usuário vazio e senha válida

**Descrição:**  
Não inserir dados de usuário, inserir senha válida e clicar em login.

**Pré-condições:**  
- Estar na página de login.

**Passos para execução:**

1. Acessar a página de login.
2. Não inserir um usuário.
3. Inserir uma senha válida.
4. Clicar no botão "Login".

**Dados de entrada:**

| Campo   | Valor        |
|---------|--------------|
| Usuário |              |
| Senha   | secret_sauce |

**Resultado Esperado:**  
Usuário deve receber uma mensagem de erro.

**Resultado Obtido:**  
Mensagem de erro exibida:  
`Epic sadface: Username is required`

**Status:** ✅ **Pass**

**Observações:**  
![Screenshot](img/Screenshot%207%20%202025-05-27%20at%203.53.57%20PM.png)

---

## ✅ Conclusão

Todos os casos de teste foram executados, com comportamentos identificados conforme esperado, exceto nos casos onde a mensagem de erro genérica não diferencia claramente erro de usuário ou senha.
