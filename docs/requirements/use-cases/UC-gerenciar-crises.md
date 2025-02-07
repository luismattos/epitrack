# **Caso de Uso: Gerenciar Crises**

## **1. Descrição Breve**
Este caso de uso descreve as operações que os usuários (pacientes e profissionais de saúde) podem realizar para registrar, visualizar, editar e excluir registros de crises epilépticas no **Epitrack**. Ele permite o acompanhamento detalhado das crises, incluindo sua duração, intensidade, sintomas e fatores desencadeantes, auxiliando no tratamento e controle da epilepsia.

---

## **2. Atores**
- **Paciente (Primário):** Usuário que registra suas crises epilépticas para monitoramento pessoal e compartilhamento com médicos.
- **Profissional de Saúde (Primário):** Médico ou responsável que pode visualizar e sugerir ajustes no tratamento com base nos registros de crises.
- **Sistema Epitrack (Secundário):** Plataforma responsável por armazenar e processar os dados das crises cadastradas.

---

## **3. Gatilhos**
O usuário acessa a tela de gerenciamento de crises.

---

## **4. Fluxo de Eventos**

### **4.1. Fluxo Básico - Criar, Visualizar, Editar e Excluir Registro de Crise**
1. O usuário acessa a seção "Gerenciar Crises" no menu do Epitrack.
2. O sistema exibe a lista de crises registradas.
3. O usuário pode realizar uma das seguintes ações:
   - **Registrar uma nova crise**
   - **Visualizar detalhes de uma crise**
   - **Editar informações de um registro de crise**
   - **Excluir um registro de crise**
4. O sistema processa a ação escolhida e atualiza a lista de crises conforme necessário.
5. O caso de uso termina quando o usuário finaliza a interação com a seção de gerenciamento de crises.

---

### **4.2. Fluxos Alternativos**

#### **4.2.1. Registrar Nova Crise**
1. O usuário seleciona a opção de registrar nova crise.
2. O sistema solicita as seguintes informações:
   - Data e horário da crise
   - Duração da crise
   - Tipo de crise
<!--
   - Sintomas observados antes, durante e após a crise
   - Possíveis gatilhos (estresse, falta de sono, luzes piscantes, etc.)
   - Intensidade da crise (leve, moderada, severa)
   - Se houve administração de medicamento emergencial
   - Observações adicionais (exemplo: contexto da crise)
-->
3. O usuário insere os dados e confirma a criação.
4. O sistema valida as informações e adiciona o registro à lista de crises.

---

#### **4.2.2. Excluir Registro de Crise**
1. O usuário seleciona um registro de crise da lista e escolhe "Excluir".
2. O sistema solicita confirmação da exclusão.
3. Após a confirmação, o registro é removido do sistema.
4. O sistema mantém um histórico anonimizado para estatísticas do usuário.

---

#### **4.2.3. Editar Registro de Crise**
1. O usuário seleciona um registro de crise e escolhe "Editar".
2. O sistema permite a edição das informações registradas, incluindo:
   - Atualização da duração, tipo, sintomas e gatilhos
   - Adição de novas observações médicas ou pessoais
3. O usuário confirma as alterações e o sistema atualiza os dados.

---

#### **4.2.4. Registrar Crise em Tempo Real**
1. O usuário acessa um botão de "Registrar Crise Agora".
2. O sistema inicia um cronômetro para marcar a duração da crise.
3. O usuário pode adicionar informações durante ou após a crise.
4. O sistema permite que o usuário finalize o registro e preencha os detalhes adicionais.

---

#### **4.2.5. Gerar Relatório de Crises**
1. O usuário seleciona a opção "Gerar Relatório".
2. O sistema permite filtros por período, tipo de crise, intensidade e gatilhos.
3. O relatório é gerado em formato PDF e pode ser compartilhado com profissionais de saúde.

---

## **5. Requisitos Especiais**
- O sistema deve permitir que o paciente visualize estatísticas sobre suas crises ao longo do tempo.
- O sistema pode sugerir padrões de crises com base nos dados coletados, auxiliando no tratamento.
- O sistema deve possibilitar exportação de registros para que o paciente possa compartilhá-los com seu médico.

---

## **6. Pré-condições**
- O usuário deve estar autenticado no sistema.
- O registro de crise deve estar cadastrado para ser editado ou excluído.

---

## **7. Pós-condições**
- **Sucesso:** A crise foi gerenciada corretamente conforme a ação escolhida.
- **Falha:** O sistema mantém a lista de crises inalterada e informa o usuário sobre qualquer erro ocorrido (exemplo: falha ao salvar dados, informações incompletas, etc.).

---

### **8. Regras de Negócio**
- [RN001](../regras-de-negocio.md)
- O sistema deve impedir exclusões acidentais de registros de crises críticas.
- Profissionais de saúde podem visualizar registros apenas com autorização do paciente.
- O sistema pode emitir alertas caso o usuário apresente um aumento na frequência das crises.
