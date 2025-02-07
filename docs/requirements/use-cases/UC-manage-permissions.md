# **UC04 - ManagePermissions**  

## **1. Descrição Breve**  
Este caso de uso descreve o processo pelo qual um usuário gerencia permissões de acesso dentro do sistema. O usuário pode conceder, modificar ou revogar permissões para outras pessoas em relação aos seus dados ou funcionalidades específicas.

---

## **2. Atores**  
- **Usuário (Primário):** Pessoa que deseja gerenciar permissões sobre seus dados.  
- **Sistema (Secundário):** Responsável por aplicar e validar as permissões definidas.  

---

## **3. Gatilhos**  
O usuário acessa a configuração de permissões e deseja modificar as regras de acesso a seus dados ou funcionalidades.  

---

## **4. Fluxo de Eventos**  

### **4.1. Fluxo Básico - Alteração de Permissão Bem-Sucedida**  
1. O usuário acessa a seção "Gerenciar Permissões".  
2. O sistema exibe a lista de usuários com permissões definidas.  
3. O usuário seleciona um contato e escolhe a permissão a ser alterada.  
4. O usuário modifica ou revoga a permissão.  
5. O sistema aplica a mudança e confirma a ação.  

---

### **4.2. Fluxos Alternativos**  

#### **4.2.1. Contato Não Encontrado**  
1. O usuário tenta modificar permissões de um contato que não está em sua lista.  
2. O sistema informa que não há permissões definidas para esse contato.  
3. O fluxo retorna ao passo 2 do fluxo básico.  

#### **4.2.2. Permissão Restrita por Política do Sistema**  
1. O usuário tenta conceder uma permissão que está bloqueada pelas regras do sistema.  
2. O sistema exibe uma mensagem informando a restrição.  
3. O fluxo retorna ao passo 2 do fluxo básico.  

---

## **5. Regras de Negócio**  

- **RN-001:** O usuário pode modificar permissões apenas para contatos existentes em sua lista.  
- **RN-002:** Certas permissões podem ser restritas pelo sistema para garantir segurança e conformidade com políticas internas.  
- **RN-003:** O usuário pode revogar permissões a qualquer momento, e a mudança deve ter efeito imediato.  

---

## **6. Pós-condições**  

- **Permissão modificada:** O contato agora possui as novas permissões definidas pelo usuário.  
- **Permissão revogada:** O contato perde o acesso às informações ou funcionalidades específicas.  
