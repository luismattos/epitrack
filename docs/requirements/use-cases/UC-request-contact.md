# **UC07 - RequestContact**  

## **1. Descrição Breve**  
Este caso de uso descreve o processo pelo qual um usuário pode enviar uma solicitação de contato para outro usuário dentro do sistema. O sistema permite que os usuários gerenciem suas conexões e definam permissões para aceitar ou rejeitar solicitações.

---

## **2. Atores**  
- **Usuário Solicitante (Primário):** Pessoa que envia a solicitação de contato.  
- **Usuário Destinatário (Secundário):** Pessoa que recebe a solicitação de contato e decide aceitar ou rejeitar.  
- **Sistema (Secundário):** Responsável por registrar e gerenciar o status das solicitações de contato.  

---

## **3. Gatilhos**  
O usuário deseja adicionar outro usuário como contato dentro do sistema e inicia a solicitação.  

---

## **4. Fluxo de Eventos**  

### **4.1. Fluxo Básico - Solicitação de Contato Bem-Sucedida**  
1. O usuário acessa a opção "Adicionar Contato".  
2. O sistema solicita um identificador do usuário destinatário (exemplo: e-mail ou nome de usuário).  
3. O usuário fornece o identificador e confirma a solicitação.  
4. O sistema verifica se o destinatário existe e permite o envio da solicitação.  
5. O sistema registra a solicitação de contato e notifica o destinatário.  

---

### **4.2. Fluxos Alternativos**  

#### **4.2.1. Usuário Destinatário Não Existe**  
1. O usuário fornece um identificador inválido.  
2. O sistema exibe uma mensagem informando que o destinatário não foi encontrado.  
3. O fluxo retorna ao passo 2 do fluxo básico.  

#### **4.2.2. Usuário Já Está Adicionado**  
1. O usuário tenta enviar uma solicitação para alguém que já está na lista de contatos.  
2. O sistema informa que o contato já foi adicionado anteriormente.  
3. O fluxo retorna ao passo 2 do fluxo básico.  

#### **4.2.3. Usuário Destinatário Rejeita a Solicitação**  
1. O usuário destinatário recebe a solicitação e opta por rejeitá-la.  
2. O sistema remove a solicitação pendente e notifica o solicitante.  

---

## **5. Regras de Negócio**  

- **RN-001:** O usuário não pode enviar solicitações para um contato já existente.  
- **RN-002:** O usuário pode cancelar uma solicitação pendente antes da resposta do destinatário.  
- **RN-003:** O usuário destinatário pode aceitar ou rejeitar uma solicitação sem que o solicitante seja notificado da rejeição.  

---

## **6. Pós-condições**  

- **Solicitação aceita:** O usuário solicitante e o destinatário agora estão conectados.  
- **Solicitação rejeitada:** O contato não foi adicionado e a solicitação foi removida do sistema.  
