# Sistema de Gestão das Olimpíadas (SGO)

Projeto desenvolvido para a disciplina de **Projeto de Software** — PUC Minas  
Professor: João Paulo Carneiro Aramuni  
Curso: Engenharia de Software — 4º Período  
Alunos: Gabriel dos Santos e Vinicius Ribeiro

---

## 📋 Descrição do Sistema

Com a chegada das Olimpíadas, o SGO é um sistema de gestão desenvolvido para coordenar os diferentes aspectos do evento. O sistema permite o gerenciamento de competições, inscrições de atletas, alocação de locais para as provas e controle de resultados.

---

## 📖 Histórias de Usuário
**US01 — Cadastrar Competição**
Como organizador das Olimpíadas, quero cadastrar novas competições com nome da modalidade, data, horário e local, para que os atletas possam se inscrever e o evento seja gerenciado corretamente.
 
**Critérios de aceitação:**
- O sistema deve exigir os campos: nome da modalidade, data, horário e local.
- Não deve ser possível cadastrar duas competições no mesmo local e horário.
- Após o cadastro, a competição deve aparecer na listagem de competições disponíveis.
- O sistema deve confirmar o cadastro com uma mensagem de sucesso.
---
 
**US02 — Editar Competição**
Como organizador, quero editar os dados de uma competição já cadastrada, para corrigir informações como data, horário ou local sem precisar excluir e recriar o registro.
 
**Critérios de aceitação:**
- Apenas competições ainda não realizadas podem ser editadas.
- A edição deve verificar conflito de horário no local antes de salvar.
- O histórico de alterações deve ser registrado com data e responsável.
- Atletas inscritos devem ser notificados em caso de mudança de data ou local.
---
 
**US03 — Listar Competições**
Como usuário do sistema, quero visualizar a lista de todas as competições cadastradas, para acompanhar o calendário de eventos das Olimpíadas.
 
**Critérios de aceitação:**
- A lista deve exibir nome da modalidade, data, horário, local e número de atletas inscritos.
- Deve ser possível filtrar por modalidade, data ou local.
- O sistema deve ordenar as competições por data em ordem cronológica por padrão.
- Competições já realizadas devem ser distinguidas visualmente das futuras.
---
 
**US04 — Inscrever Atleta em Competição**
Como representante de delegação, quero inscrever um atleta em uma competição específica, para que ele possa participar oficialmente da modalidade representando seu país.
 
**Critérios de aceitação:**
- O atleta deve estar previamente cadastrado no sistema.
- Cada atleta só pode representar um país por modalidade.
- O sistema deve impedir inscrição duplicada do mesmo atleta na mesma competição.
- Deve ser possível inscrever o mesmo atleta em competições de modalidades diferentes.
---
 
**US05 — Cancelar Inscrição de Atleta**
Como representante de delegação, quero cancelar a inscrição de um atleta em uma competição, para atualizar o quadro de participantes quando necessário.
 
**Critérios de aceitação:**
- O cancelamento só é permitido antes do início da competição.
- O sistema deve confirmar a ação antes de efetivar o cancelamento.
- A vaga liberada deve estar disponível para novos atletas imediatamente.
- O histórico de inscrição cancelada deve ser mantido para fins de auditoria.
---
 
**US06 — Cadastrar Atleta**
Como administrador do sistema, quero cadastrar novos atletas com nome, país de origem e data de nascimento, para que estejam aptos a se inscrever em competições.
 
**Critérios de aceitação:**
- Os campos obrigatórios são: nome completo, país de origem e data de nascimento.
- Não deve ser permitido o cadastro de atletas duplicados (mesmo nome e país).
- O sistema deve validar que o atleta tem idade mínima conforme a modalidade.
- Após o cadastro, o atleta deve estar disponível para inscrição imediatamente.
---
 
**US07 — Consultar Perfil de Atleta**
Como usuário, quero consultar o perfil de um atleta, para visualizar suas informações pessoais, país representado e competições em que está inscrito.
 
**Critérios de aceitação:**
- O perfil deve exibir nome, país, data de nascimento e modalidades cadastradas.
- Deve listar todas as competições em que o atleta está inscrito ou já participou.
- Deve exibir o histórico de medalhas conquistadas pelo atleta.
- A consulta deve ser acessível por nome ou código do atleta.
---
 
**US08 — Alocar Local para Competição**
Como organizador, quero alocar um local específico para uma competição, para garantir que o espaço esteja reservado na data e horário corretos sem conflito com outros eventos.
 
**Critérios de aceitação:**
- O sistema deve verificar se o local já está ocupado no horário solicitado.
- Caso haja conflito, o sistema deve exibir a competição que já ocupa o horário.
- A alocação só pode ser feita para locais cadastrados e ativos no sistema.
- Após a alocação, o local deve aparecer como indisponível para o mesmo horário.
---
 
**US09 — Cadastrar Local**
Como administrador, quero cadastrar locais disponíveis para as competições informando nome, capacidade e endereço, para que possam ser alocados aos eventos.
 
**Critérios de aceitação:**
- Os campos obrigatórios são: nome do local, capacidade máxima e endereço.
- Não deve ser permitido o cadastro de locais com o mesmo nome.
- O local deve estar disponível para alocação imediatamente após o cadastro.
- O sistema deve permitir marcar um local como inativo para manutenção.
---
 
**US10 — Verificar Disponibilidade de Local**
Como organizador, quero consultar a disponibilidade de um local em uma data e horário específicos, para planejar a alocação de competições sem gerar conflitos.
 
**Critérios de aceitação:**
- O sistema deve exibir a agenda completa do local com competições já alocadas.
- Deve indicar claramente os horários livres e ocupados.
- O resultado deve poder ser filtrado por data ou período.
- A consulta deve refletir as alocações mais recentes em tempo real.
---
 
**US11 — Registrar Resultado de Competição**
Como árbitro, quero registrar os resultados de uma competição após sua realização indicando os atletas classificados em 1º, 2º e 3º lugar, para que as medalhas sejam atribuídas corretamente.
 
**Critérios de aceitação:**
- Os resultados só podem ser registrados após o horário de início da competição.
- Devem ser informados obrigatoriamente os atletas em 1º, 2º e 3º lugar.
- Os atletas selecionados devem estar inscritos na competição.
- Após o registro, as medalhas devem ser automaticamente computadas no relatório do país.
---
 
**US12 — Consultar Resultado de Competição**
Como usuário, quero consultar os resultados de uma competição já realizada, para saber quais atletas foram classificados e as medalhas conquistadas.
 
**Critérios de aceitação:**
- O resultado deve exibir os atletas em 1º, 2º e 3º lugar com seus respectivos países.
- Deve indicar a data, horário e local em que a competição foi realizada.
- Competições sem resultado registrado devem ser identificadas como "pendente".
- A consulta deve estar disponível para qualquer usuário sem autenticação especial.
---
 
**US13 — Gerar Relatório de Medalhas por País**
Como organizador, quero visualizar o quadro de medalhas com o desempenho de cada país, para acompanhar o ranking das delegações nas Olimpíadas.
 
**Critérios de aceitação:**
- O relatório deve exibir o total de medalhas de ouro, prata e bronze por país.
- O ranking deve ser ordenado por: ouro, depois prata, depois bronze.
- Deve ser possível exportar o relatório em formato PDF ou planilha.
- O relatório deve ser atualizado automaticamente após cada resultado registrado.
---
 
**US14 — Filtrar Relatório de Medalhas**
Como usuário, quero filtrar o quadro de medalhas por modalidade ou período, para analisar o desempenho das delegações em categorias específicas.
 
**Critérios de aceitação:**
- Deve ser possível filtrar por modalidade esportiva.
- Deve ser possível filtrar por período (data de início e fim).
- A aplicação de filtros deve atualizar o relatório em tempo real.
- Deve existir opção para limpar todos os filtros e voltar à visão geral.
---
 
**US15 — Autenticar Usuário no Sistema**
Como usuário, quero realizar login com minhas credenciais, para acessar as funcionalidades de acordo com meu perfil de permissão.
 
**Critérios de aceitação:**
- O sistema deve autenticar por e-mail e senha.
- Usuários com perfil "visualizador" só podem consultar dados, sem permissão para cadastro ou edição.
- Usuários com perfil "organizador" podem gerenciar competições, inscrições e resultados.
- Apenas administradores podem cadastrar locais, atletas e gerenciar usuários do sistema.
- Após 3 tentativas incorretas de login, a conta deve ser temporariamente bloqueada.
---

## 📊 Diagramas

### Diagrama de Caso de Uso
<img width="500px" height="500px" src="https://github.com/Gb1201/gabriel_vini-sistema-gestao-olimpiadas/blob/main/imagens/diagrama-de-caso-de-uso.png"/>

### Diagrama de Classes
<img width="500px" height="500px" src="https://github.com/Gb1201/gabriel_vini-sistema-gestao-olimpiadas/blob/main/imagens/DiagramaDeClasses_Olimpiadas.png"/>

### Diagrama de Pacotes
<img width="500px" height="500px" src="https://github.com/Gb1201/gabriel_vini-sistema-gestao-olimpiadas/blob/main/imagens/DiagramaDePacotes_Olimpiadas.png"/>

### Diagrama de Componentes
<img width="500px" height="500px" src="https://github.com/Gb1201/gabriel_vini-sistema-gestao-olimpiadas/blob/main/imagens/diagrama-de-componentes.png"/>

### Diagrama de Implantação
<img width="500px" height="500px" src="https://github.com/Gb1201/gabriel_vini-sistema-gestao-olimpiadas/blob/main/imagens/DiagramaDeImplantacao_Olimpiadas.png"/>

---

## 📁 Estrutura do Repositório

```
├── codigos/
│   ├── diagrama-caso-de-uso.puml
│   ├── diagrama-de-classes.puml
│   ├── diagrama-de-pacotes.puml
│   ├── diagrama-de-componentes.puml
│   └── diagrama-de-implantação.puml
├── imagens/
    ├── diagrama-de-caso-de-uso.png
    ├── diagrama-de-componentes.png
│   ├── DiagramaDeClasses_Olimpiadas.png
│   ├── DiagramaDePacotes_Olimpiadas.png
│   └── DiagramaDeImplantacao_Olimpiadas.png
└── README.md
```

---

## 🛠️ Tecnologias Utilizadas

- [PlantUML](https://plantuml.com/) — modelagem dos diagramas UML
- [API  PlantUML](https://github.com/joaopauloaramuni/python/tree/main/PROJETOS/Projeto%20PlantUML%20API/plantuml_code) — APIs do PlantUML que foram usadas como base
