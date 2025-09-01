# Especificações do Projeto

<!--
<span style="color:red">Pré-requisitos: <a href="1-Documentação de Contexto.md"> Documentação de Contexto</a></span>

Definição do problema e ideia de solução a partir da perspectiva do usuário. É composta pela definição do  diagrama de personas, histórias de usuários, requisitos funcionais e não funcionais além das restrições do projeto.

Apresente uma visão geral do que será abordado nesta parte do documento, enumerando as técnicas e/ou ferramentas utilizadas para realizar a especificações do projeto
-->

## Personas

| **Nome**           | **Idade** | **Profissão**              | **Frustrações**                                                                 | **Expectativas**                                                                |
|--------------------|-----------|----------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| **João Souza**     | 35        | Administrador do Estabelecimento	 | Sentimento de impotência: Não ter controle ou visibilidade sobre a operação quando está fora do escritório, dependendo de ligações para saber o que está acontecendo. Perda de tempo e dinheiro: Gastar horas preciosas em trocas de mensagens para resolver conflitos de agenda e perder receita com "no-shows" que não puderam ser rapidamente remanejados. | Ter uma visão geral dos agendamentos e faturamento no celular. Gerenciar a agenda de múltiplos profissionais de forma remota.|
| **Mariana Ferreira**| 28        | Profissional / Prestador de Serviço	     | Falhas de comunicação: Ser pego de surpresa por um agendamento ou cancelamento que foi comunicado por e-mail e não visto a tempo, gerando despreparo ou tempo ocioso. Falta de autonomia: A dificuldade de gerenciar a própria agenda em tempo real, como bloquear um horário para um imprevisto, dependendo de outra pessoa para acessar o sistema principal. Quebra do fluxo de trabalho: Ter que interromper um atendimento para responder mensagens sobre agendamentos ou consultar informações sobre o próximo cliente. 	| Visualizar sua agenda em tempo real no app. Receber notificações push sobre novos agendamentos ou cancelamentos. Bloquear horários na sua agenda de forma rápida pelo celular. |
| **Lucas Almeida**  | 42        | Cliente B2B (Empresa Contratante)	 | Processo lento e burocrático: A enorme perda de tempo com a troca interminável de e-mails e ligações ("pingue-pongue") apenas para encontrar um horário compatível. Dependência e rigidez: Sentir-se preso ao horário comercial da empresa prestadora para conseguir agendar ou, pior, para alterar um compromisso urgente. Experiência frustrante: A péssima impressão causada por sites que não funcionam bem no celular ou pela falta de uma confirmação instantânea, o que gera insegurança e passa uma imagem de desorganização da empresa contratada.  | Encontrar horários disponíveis e agendar um serviço em poucos toques. Receber confirmações e lembretes via notificação push. Poder reagendar ou cancelar compromissos diretamente pelo aplicativo. |



## Histórias de Usuários

| **Persona**           | **Como**                                    | **Quero**                                                 | **Para Que**                                               |
|-----------------------|---------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------|
| **João Souza**| 35| Administrador do Estabelecimento|  Visualizar um dashboard simplificado no meu celular com os principais indicadores do dia.| Tomar decisões rápidas mesmo estando fora do escritório.   |
| **Kleber Machado**| 42 | Médico |  Receber uma notificação push instantânea quando um cliente agendar um horário comigo.  | Me preparar para o atendimento com antecedência.  |
| **Mariana Ferreira**| 28| Dona de empresa| Poder buscar um serviço e agendá-lo em menos de 2 minutos pelo aplicativo. | Otimizar meu tempo e resolver essa demanda rapidamente. |
| **Lucas Almeida**| 39| Personal trainer | Receber um lembrete no meu celular um dia antes do compromisso. |  Não esquecer e evitar problemas de não comparecimento. |
| **Pedro Santos**| 50| Autônomo | Cadastrar um novo serviço ou profissional diretamente pelo aplicativo. |  Manter a plataforma sempre atualizada sem precisar de um computador. |
|


<!--
Apresente aqui as histórias de usuário que são relevantes para o projeto de sua solução. As Histórias de Usuário consistem em uma ferramenta poderosa para a compreensão e elicitação dos requisitos funcionais e não funcionais da sua aplicação. Se possível, agrupe as histórias de usuário por contexto, para facilitar consultas recorrentes à essa parte do documento.
-->
## Requisitos
<!--
As tabelas que se seguem apresentam os requisitos funcionais e não funcionais que detalham o escopo do projeto.
-->
### Requisitos Funcionais

|ID    | Descrição do Requisito  | Prioridade |
|------|-----------------------------------------|----|
|**RF-001**| <div align=center>Agendamento Rápido: O sistema deve permitir que um Cliente B2B conclua um agendamento em, no máximo, 5 etapas dentro do aplicativo.	</div> | ALTA | 
|**RF-002**| <div align=center>Gestão de Agendas Multi-Profissional: O Administrador deve poder visualizar e filtrar as agendas de todos os profissionais cadastrados em uma única tela móvel.	</div>  | ALTA |
|**RF-003**| <div align=center>Sistema de Notificações Push: O app deve enviar notificações automáticas para confirmação, lembrete (24h antes), alteração e cancelamento de agendamentos para todos os perfis.	</div>  | ALTA |
|**RF-004**| <div align=center>Perfis de Usuário e Autenticação: O sistema deve ter um processo de cadastro/login seguro (e-mail/senha, Google) e diferenciar as permissões de cada perfil.	</div>  | MÉDIA |
|**RF-005**| <div align=center>Dashboard Gerencial Móvel: O Administrador deve ter acesso a um painel visual com métricas chave (agendamentos do dia, receita prevista, etc.).	</div> | MÉDIA |
|**RF-006**| <div align=center>Gerenciamento de Serviços pelo App: O Administrador deve poder criar, editar e desativar serviços (nome, duração, preço) diretamente da interface do aplicativo.	</div> | MÉDIA |


### Requisitos Não Funcionais  

| ID       | Descrição do Requisito  | Prioridade |
|----------|-------------------------|------------|
| **RNF-001** | Segurança: A comunicação entre o app e o servidor deve ser criptografada (SSL/TLS). Dados sensíveis devem ser armazenados de forma segura, em conformidade com a LGPD.	| ALTA |
| **RNF-002** | Desempenho: O tempo de carregamento da tela principal e da agenda não deve exceder 2 segundos em uma conexão 4G estável.	 | ALTA |
| **RNF-003** | Usabilidade (UI/UX): A interface deve ser intuitiva, limpa e seguir as diretrizes de design nativas do Android (Material Design).	 | ALTA |
| **RNF-004** | Compatibilidade: O aplicativo deve ser compatível com as duas últimas versões principais do sistema operacionaL Android.	| ALTA |
| **RNF-005** | Consumo de Recursos: O aplicativo deve ser otimizado para minimizar o consumo de bateria e de dados móveis em segundo plano.	 | MÉDIA |




## Restrições

O projeto está restrito pelos itens apresentados na tabela a seguir.

|ID| Restrição                                             |
|--|-------------------------------------------------------|
|**R-01**| Os usuários precisam ter mais de 18 anos para utilizar a plataforma. |
|**R-02**| É necessário se cadastrar para utilizar a plataforma. |
|**R-03**| O usuário precisa fornecer o seu CPF para poder concluir o cadastro. |
|**R-04**| Não é possível utilizar palavras de baixo calão na plataforma. |
|**R-05**| É necessário verificar o e-mail para concluir o cadastro. |



