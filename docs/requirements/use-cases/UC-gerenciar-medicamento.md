# **Caso de Uso: Gerenciar Medicamentos**

## **1. Descrição Breve**
Este caso de uso descreve as operações que os usuários (pacientes e profissionais de saúde) podem realizar para cadastrar, visualizar, editar, excluir e acompanhar a administração de medicamentos no **Epitrack**. Ele permite o registro detalhado da medicação, frequência de uso e horários de administração, auxiliando no controle e adesão ao tratamento.

---

## **2. Atores**
- **Paciente (Primário):** Usuário que gerencia seus próprios medicamentos e administrações.
- **Profissional de Saúde (Primário):** Médico ou responsável que pode visualizar e sugerir ajustes no tratamento medicamentoso.
- **Sistema Epitrack (Secundário):** Plataforma responsável por armazenar e processar os dados dos medicamentos cadastrados.

---

## **3. Gatilhos**
O usuário inicia a operação explicitamente acessando a seção "Gerenciar Medicamentos" no sistema Epitrack.

---

## **4. Fluxo de Eventos**

### **4.1. Fluxo Básico - Criar, Visualizar, Editar e Excluir Medicamento**
1. O usuário acessa a seção "Gerenciar Medicamentos" no menu do Epitrack.
2. O sistema exibe a lista de medicamentos cadastrados.
3. O usuário pode realizar uma das seguintes ações:
   - **Criar um novo medicamento**
   - **Visualizar detalhes de um medicamento**
   - **Editar informações de um medicamento**
   - **Excluir um medicamento**
   - **Registrar uma administração de medicamento**
4. O sistema processa a ação escolhida e atualiza a lista de medicamentos conforme necessário.
5. O caso de uso termina quando o usuário finaliza a interação com a seção de gerenciamento de medicamentos.

---

### **4.2. Fluxos Alternativos**
#### **4.2.1. Criar Novo Medicamento**
1. O usuário seleciona a opção "Adicionar Medicamento".
2. O sistema solicita as seguintes informações:
   - Nome do medicamento
   - Dosagem
   - Forma de administração (oral, injetável, etc.)
   - Frequência (quantidade de vezes ao dia, semana, etc.)
   - Horários específicos de administração
   - Observações médicas (se necessário)
3. O usuário insere os dados e confirma a criação.
4. O sistema valida as informações e adiciona o medicamento à lista.

---

#### **4.2.2. Excluir Medicamento**
1. O usuário seleciona um medicamento da lista e escolhe "Excluir".
2. O sistema solicita confirmação da exclusão.
3. Após a confirmação, o medicamento é removido do sistema.
4. O sistema mantém um registro no histórico, evitando a perda de informações importantes.

---

#### **4.2.3. Editar Medicamento**
1. O usuário seleciona um medicamento e escolhe "Editar".
2. O sistema permite a edição das informações, incluindo:
   - Nome, dosagem, forma de administração e frequência
   - Atualização de horários e ajustes conforme orientação médica
3. O usuário confirma as alterações e o sistema atualiza os dados.

---

#### **4.2.4. Registrar Administração de Medicamento**
1. O usuário acessa um medicamento e seleciona "Registrar Administração".
2. O sistema permite que o usuário insira:
   - Data e hora da administração
   - Observações opcionais (efeitos colaterais, sintomas)
3. O sistema registra a administração e exibe um histórico de todas as administrações do medicamento.
4. Se o usuário esqueceu uma dose, pode registrar a administração retroativamente.

---

#### **4.2.5. Alertas e Notificações**
1. O sistema verifica a frequência e os horários cadastrados para cada medicamento.
2. Quando chega o horário programado, o sistema envia uma notificação ao usuário via:
   - Notificação push (app)
   - E-mail (se configurado)
3. O usuário pode confirmar a administração ou postergar o lembrete.
4. O sistema registra a ação no histórico.

---

## **5. Requisitos Especiais**
- O sistema deve validar que medicamentos não podem ser cadastrados em duplicidade para o mesmo período sem uma justificativa.
- Alertas devem ser configuráveis para lembrar o usuário sobre a administração da medicação.
- O histórico de medicamentos administrados deve estar disponível para consulta.
- O sistema deve permitir que profissionais de saúde façam sugestões de ajuste nos medicamentos cadastrados pelo paciente.

---

## **6. Pré-condições**
- O usuário deve estar autenticado no sistema.
- O medicamento deve estar cadastrado para ser editado, excluído ou administrado.

---

## **7. Pós-condições**
- **Sucesso:** O medicamento foi gerenciado corretamente conforme a ação escolhida.
- **Falha:** O sistema mantém a lista de medicamentos inalterada e informa o usuário sobre qualquer erro ocorrido (exemplo: falha ao salvar dados, horários conflitantes, etc.).

---

### **8. Regras de Negócio**
- O sistema deve impedir exclusões acidentais de medicamentos que possuem histórico de administração.
- Usuários podem visualizar e editar apenas seus próprios medicamentos, exceto quando autorizados por um profissional de saúde.
- O sistema deve permitir exportação do histórico de medicamentos em formato PDF para compartilhamento com médicos.
