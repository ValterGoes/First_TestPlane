
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
![Screenshot](attachment:b3df8b7a-837d-428c-9d25-384952884858:Screenshot_2025-05-27_at_3.13.50_PM.png)

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
![Screenshot](attachment:e78e106d-0056-4503-a7d2-099ff7f68250:Screenshot_2025-05-27_at_3.28.03_PM.png)

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
![Screenshot](attachment:e14799e8-c649-498b-9bd0-8d317f337d4b:Screenshot_2025-05-27_at_3.34.37_PM.png)

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
![Screenshot](attachment:7ba8ec69-809e-4e04-a834-b5432fb94eaa:Screenshot_2025-05-27_at_3.39.02_PM.png)

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
![Screenshot](attachment:dcb4d312-726c-425a-9172-082b1fc3fe50:Screenshot_2025-05-27_at_3.43.04_PM.png)

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
![Screenshot](attachment:b5f2d935-bd65-4cbb-b3a7-3e091a737565:Screenshot_2025-05-27_at_3.48.33_PM.png)

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
![Screenshot](attachment:bc9fdb3c-0b76-4c56-b3c6-bdb158ae6a08:Screenshot_2025-05-27_at_3.53.57_PM.png)

---

## ✅ Conclusão

Todos os casos de teste foram executados, com comportamentos identificados conforme esperado, exceto nos casos onde a mensagem de erro genérica não diferencia claramente erro de usuário ou senha.
