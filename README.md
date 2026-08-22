# Documentação de resquisitos para o sistema Devisate construções 

## Integrantes: Maria Eduarda Durães Cruz Mesquita e Maria Eduarda Rangel Sousa 


##### Este documento apresenta o levantamento de requisitos do sistema Devisste construções, com o objetivo de informar o controle de requisitos de equipamentos, empréstimos, agendamentos e manunteções da empresa. 

#### situação problema:

##### A empresa Devisate Construções possui diversos equipamentos utilizados em obras e atividades de manutenção. Atualmente, o controle desses equipamentos é realizado de forma manual, por meio de anotações, panilhas e mensagens de aplicativos de conversa. Com o aumento da quantidade de equipamentos, essa forma de controle passou a apresentar diversos problemas, entre eles: equipamentos emprestados sem registro formal, dificuldade em localizar materiais, conflitos de agendamento entre obras, falta de histórico de manutenção, ausência de indicadores gerenciais e falta de controle sobre os responsáveis por cada equipamento em uso.

##### Para atender às necessidades apresentadas, o sistema foi organizado em três áreas principais, descritas a seguir. 

#### Área Pública 

##### Composta pela página inicial, pela seção sobre a empresa, pelo catálogo de equipamentos e pela tela de login. 

#### Área do Usuário 

##### Composta pelo perfil do usuário, pela solicitação de equipamentos, pelo histórico de empréstimos e pelo histórico de agendamentos. 

#### Área Administrativa 

##### Composta pelo dashboard, pelo cadastro de usuários, categorias e equipamentos, pelo controle de empréstimos e devoluções, pelo módulo de manutenções e pela geração de relatórios. 

### Requisitos Funcionais 

##### Os requisitos funcionais descrevem as ações que o sistema deve executar, sempre associadas a um ator responsável, seja ele o usuário, o operador, o técnico ou o administrador. 

##### RF01 – O sistema deve permitir que o usuário realize login informando e-mail e senha cadastrados previamente. 

##### RF02 – O sistema deve permitir que o usuário recupere sua senha por meio de um link enviado ao e-mail cadastrado. 

##### RF03 – O administrador deve conseguir cadastrar novos usuários, definindo o perfil de acesso (funcionário, responsável de obra ou administrador). 

##### RF04 – O administrador deve conseguir editar ou desativar o cadastro de um usuário existente. 

##### RF05 – O administrador deve conseguir cadastrar categorias de equipamentos, como compactação, elevação e concretagem, para organizar o catálogo. 

##### RF06 – O administrador deve conseguir cadastrar categorias de manutenção, separando-as em corretiva e preventiva. 

##### RF07 – O administrador deve conseguir cadastrar um novo equipamento informando número de série, categoria, horímetro/odômetro inicial e status de disponibilidade. 

##### RF08 – O sistema deve permitir a consulta do catálogo de equipamentos filtrando por categoria e por status (disponível, alugado, em manutenção, reservado). 

##### RF09 – O sistema deve exibir, na ficha de cada equipamento, o histórico de empréstimos e manutenções já realizados. 

##### RF10 – O usuário deve conseguir solicitar o agendamento de um equipamento informando período desejado, obra de destino e finalidade de uso. 

##### RF11 – O operador deve conseguir aprovar ou recusar uma solicitação de agendamento pendente. 

##### RF12 – O sistema deve impedir que um equipamento em manutenção ou já reservado seja agendado para o mesmo período por outro usuário. 

##### RF13 – O operador deve conseguir registrar a retirada de um equipamento, vinculando-o ao usuário responsável e à obra de destino. 

##### RF14 – O operador deve conseguir anexar fotos do equipamento no checklist de retirada, registrando eventuais avarias existentes. 

##### RF15 – O operador deve conseguir registrar a devolução de um equipamento, comparando o checklist de saída com o checklist de retorno. 

##### RF16 – O sistema deve calcular automaticamente eventuais multas por atraso na devolução, com base na data prevista e na data efetiva de retorno. 

##### RF17 – O técnico deve conseguir abrir uma Ordem de Serviço para um equipamento, classificando-a como corretiva ou preventiva. 

##### RF18 – O sistema deve alterar automaticamente o status do equipamento para "em manutenção" quando uma Ordem de Serviço for aberta para ele. 

##### RF19 – O sistema deve gerar um alerta de manutenção preventiva quando o horímetro do equipamento atingir o limite configurado. 

##### RF20 – O técnico deve conseguir registrar o encerramento de uma Ordem de Serviço, informando peças utilizadas, mão de obra e custo total do serviço. 

##### RF21 – O administrador deve conseguir visualizar, no dashboard, indicadores de equipamentos disponíveis, alugados e em manutenção em tempo real. 

##### RF22 – O sistema deve exibir, no dashboard, um ranking dos equipamentos mais utilizados e das obras com maior volume de locações. 

##### RF23 – O administrador deve conseguir gerar relatórios de utilização de equipamentos e de custos de manutenção por período. 

##### RF24 – O administrador deve conseguir configurar os valores de tarifa de locação, sendo eles diária, semanal, quinzenal e mensal, para cada equipamento. 

##### RF25 – O usuário deve conseguir consultar, em seu perfil, o histórico completo de empréstimos e agendamentos já realizados. 

### Requisitos Não Funcionais 

##### Os requisitos não funcionais descrevem as condições de qualidade, segurança, desempenho e usabilidade que o sistema deve atender enquanto executa as funções descritas na seção anterior. 

##### RNF01 – O sistema deve armazenar as senhas dos usuários de forma criptografada, nunca em texto puro. 

##### RNF02 – O sistema deve impedir o acesso de usuários não autenticados às páginas da área administrativa. 

##### RNF03 – O sistema deve carregar o catálogo de equipamentos e o dashboard em até três segundos em condições normais de rede. 

##### RNF04 – O sistema deve ser responsivo, permitindo que operadores registrem retiradas e devoluções corretamente a partir de celulares e tablets no canteiro de obra. 

##### RNF05 – O sistema deve manter um registro de auditoria de todas as alterações de status dos equipamentos, com data, hora e usuário responsável. 

##### RNF06 – O sistema deve estar disponível para consulta e registro de operações em pelo menos 99% do tempo mensal. 

##### RNF07 – A interface deve seguir um padrão visual consistente entre a área pública, a área do usuário e a área administrativa. 

##### RNF08 – O sistema deve funcionar corretamente nos navegadores Google Chrome, Firefox e Edge em suas versões mais recentes. 

##### RNF09 – O sistema deve realizar backup automático diário da base de dados de equipamentos, contratos e manutenções. 

##### RNF10 – O sistema deve suportar o cadastro de pelo menos 5.000 equipamentos e 500 usuários simultâneos sem perda perceptível de desempenho. 

##### Este levantamento reúne 25 requisitos funcionais e 10 requisitos não funcionais, cobrindo os módulos de login, usuários, categorias, equipamentos, agendamentos, empréstimos, devoluções, manutenções, dashboard e administração. Cada requisito foi redigido de forma específica e testável, de modo que seja possível verificar, durante a fase de validação, se o sistema o atende ou não. Os requisitos aqui apresentados servem de base para a modelagem do banco de dados, a definição das telas e o planejamento das próximas etapas de desenvolvimento do sistema Devisate Construções. 
