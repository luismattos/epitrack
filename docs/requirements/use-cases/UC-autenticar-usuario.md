# **UC01 - AuthenticateUser**

## **1. Descrição Breve**  
Este caso de uso descreve o processo de autenticação do usuário no sistema. O usuário pode fornecer credenciais para acessar funcionalidades restritas, recuperar o acesso caso tenha esquecido a senha ou cadastrar uma nova conta. O sistema valida as credenciais e concede ou nega o acesso.

---

## **2. Atores**  
- **Usuário (Primário):** Pessoa que deseja se autenticar no sistema.  
- **Sistema (Secundário):** Responsável por validar as credenciais e gerenciar a autenticação.  

---

## **3. Gatilhos**  
O usuário tenta acessar uma funcionalidade protegida do sistema, seleciona a opção de login ou deseja criar uma nova conta.  

---

## **4. Fluxo de Eventos**  

### **4.1. Fluxo Básico - Autenticação Bem-Sucedida**  
1. O usuário acessa a tela de login.  
2. O sistema solicita as credenciais do usuário.  
3. O usuário fornece um identificador (e-mail ou nome de usuário) e senha.  
4. O sistema valida as credenciais:  
   4.1. O sistema verifica se o identificador está registrado.  
   4.2. O sistema verifica se a senha fornecida corresponde à armazenada para esse identificador.  
5. O sistema concede acesso ao usuário e redireciona para a tela inicial.  

---

### **4.2. Fluxos Alternativos**  

#### **4.2.1. Credenciais Inválidas**  
1. O usuário insere credenciais inválidas.  
2. O sistema exibe uma mensagem informando que o login falhou.  
3. O fluxo retorna ao passo 2 do fluxo básico.  

#### **4.2.2. Esqueci Minha Senha**  
1. O usuário seleciona a opção "Esqueci minha senha".  
2. O sistema solicita o e-mail ou identificador do usuário.  
3. O usuário fornece as informações solicitadas.  
4. O sistema envia um link de redefinição de senha para o e-mail cadastrado.  
5. O fluxo retorna ao passo 2 do fluxo básico após a redefinição da senha.  

#### **4.2.3. Tentativas Múltiplas de Login Mal-Sucedidas**  
1. O usuário insere credenciais inválidas repetidamente.  
2. O sistema bloqueia temporariamente a conta após um número definido de tentativas falhas.  
3. O sistema exibe uma mensagem informando sobre o bloqueio e orientando o usuário a redefinir a senha.  

#### **4.2.4. Cadastrar Nova Conta**  
1. O usuário seleciona a opção "Criar Nova Conta".  
2. O sistema solicita as seguintes informações:  
   - Nome completo  
   - E-mail  
   - Nome de usuário (se aplicável)  
   - Senha e confirmação de senha  
3. O usuário preenche os dados e confirma o cadastro.  
4. O sistema valida as informações:  
   4.1. Verifica se o e-mail ou nome de usuário já está em uso.  
   4.2. Valida se a senha atende aos requisitos mínimos de segurança.  
5. O sistema cria a nova conta e envia um e-mail de confirmação (se necessário).  
6. O sistema redireciona o usuário para a tela de login.  

---

## **5. Regras de Negócio**  

- **RN-001:** O sistema deve validar as credenciais comparando o identificador e a senha com os dados armazenados.  
- **RN-002:** Após 5 tentativas consecutivas de login mal-sucedidas, a conta deve ser temporariamente bloqueada por 10 minutos.  
- **RN-003:** A senha deve atender aos critérios de segurança definidos pelo sistema (exemplo: mínimo de 8 caracteres, pelo menos um número e um caractere especial).  
- **RN-004:** Caso a conta esteja bloqueada, o usuário deve aguardar o tempo estipulado ou redefinir sua senha para recuperar o acesso.  
- **RN-005:** O nome de usuário e o e-mail devem ser únicos no sistema.  
- **RN-006:** O sistema pode exigir confirmação de e-mail antes de permitir o primeiro login.  

---

## **6. Pós-condições**  

- **Sucesso:** O usuário é autenticado e pode acessar as funcionalidades restritas do sistema.  
- **Falha:** O sistema impede o acesso e exibe mensagens apropriadas conforme os fluxos alternativos.  
- **Cadastro bem-sucedido:** A conta foi criada e está pronta para uso após a confirmação necessária.  
