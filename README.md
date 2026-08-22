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

#### Classificação dos Requisitos 

##### Para separar os requisitos entre funcionais e não funcionais, o grupo utilizou o seguinte critério: se o requisito descreve uma ação que pode ser observada na tela, como um cadastro, uma consulta, uma aprovação ou um cálculo, ele foi classificado como funcional. Se o requisito descreve uma condição de qualidade que só é percebida quando falha, como lentidão, insegurança ou incompatibilidade com dispositivos móveis, ele foi classificado como não funcional. Esse critério foi aplicado individualmente a cada requisito listado nas seções seguintes, e a justificativa correspondente é apresentada logo após cada um deles. 

### Requisitos Funcionais 

##### Os requisitos funcionais descrevem as ações que o sistema deve executar, sempre associadas a um ator responsável, seja ele o usuário, o operador, o técnico ou o administrador. Após cada requisito, apresenta-se a justificativa de sua classificação. 

##### RF01 – O sistema deve permitir que o usuário realize login informando e-mail e senha cadastrados previamente.  
###### Justificativa: é funcional porque descreve uma ação concreta e visível — o usuário informa dados e o sistema autentica o acesso. 

##### RF02 – O sistema deve permitir que o usuário recupere sua senha por meio de um link enviado ao e-mail cadastrado.  
###### Justificativa: é funcional porque representa uma operação executada pelo sistema (gerar e enviar o link), e não uma característica de qualidade. 

##### RF03 – O administrador deve conseguir cadastrar novos usuários, definindo o perfil de acesso (funcionário, responsável de obra ou administrador).  
###### Justificativa: é funcional porque é uma ação de cadastro realizada por um ator específico, o administrador. 

##### RF04 – O administrador deve conseguir editar ou desativar o cadastro de um usuário existente.  
###### Justificativa: é funcional porque descreve uma operação de manutenção de dados que pode ser observada na tela como uma ação do usuário administrador. 

##### RF05 – O administrador deve conseguir cadastrar categorias de equipamentos, como compactação, elevação e concretagem, para organizar o catálogo.  
###### Justificativa: é funcional porque é uma ação de cadastro, não uma condição de qualidade do sistema. 

##### RF06 – O administrador deve conseguir cadastrar categorias de manutenção, separando-as em corretiva e preventiva.  
###### Justificativa: é funcional pelo mesmo motivo do requisito anterior: trata-se de uma ação de cadastro executada pelo administrador. 

##### RF07 – O administrador deve conseguir cadastrar um novo equipamento informando número de série, categoria, horímetro/odômetro inicial e status de disponibilidade. 
###### Justificativa: é funcional porque descreve uma ação concreta de entrada de dados no sistema. 

##### RF08 – O sistema deve permitir a consulta do catálogo de equipamentos filtrando por categoria e por status (disponível, alugado, em manutenção, reservado).  
###### Justificativa: é funcional porque a consulta e o filtro são ações que o usuário vê o sistema executar na tela. 

##### RF09 – O sistema deve exibir, na ficha de cada equipamento, o histórico de empréstimos e manutenções já realizados.  
###### Justificativa: é funcional porque "exibir informações" é um comportamento visível e testável do sistema, não uma qualidade transversal. 

##### RF10 – O usuário deve conseguir solicitar o agendamento de um equipamento informando período desejado, obra de destino e finalidade de uso.  
###### Justificativa: é funcional porque é uma ação executada pelo ator usuário, com dados de entrada bem definidos. 

##### RF11 – O operador deve conseguir aprovar ou recusar uma solicitação de agendamento pendente.  
###### Justificativa: é funcional porque descreve uma decisão/ação tomada por um ator específico, o operador, sobre um registro do sistema. 

##### RF12 – O sistema deve impedir que um equipamento em manutenção ou já reservado seja agendado para o mesmo período por outro usuário.  
###### Justificativa: é funcional, e não uma regra de qualidade, porque descreve uma regra de negócio que altera o comportamento do sistema em uma ação específica (o agendamento). 

##### RF13 – O operador deve conseguir registrar a retirada de um equipamento, vinculando-o ao usuário responsável e à obra de destino.  
###### Justificativa: é funcional porque é uma ação de registro de dados realizada pelo operador. 

##### RF14 – O operador deve conseguir anexar fotos do equipamento no checklist de retirada, registrando eventuais avarias existentes.  
###### Justificativa: é funcional porque "anexar" e "registrar" são ações concretas executadas na interface pelo operador. 

##### RF15 – O operador deve conseguir registrar a devolução de um equipamento, comparando o checklist de saída com o checklist de retorno.  
###### Justificativa: é funcional porque descreve uma operação específica do módulo de devoluções, executada pelo operador. 

##### RF16 – O sistema deve calcular automaticamente eventuais multas por atraso na devolução, com base na data prevista e na data efetiva de retorno. 
###### Justificativa: é funcional porque "calcular" é uma operação que o sistema executa e cujo resultado pode ser verificado (testado). 

##### RF17 – O técnico deve conseguir abrir uma Ordem de Serviço para um equipamento, classificando-a como corretiva ou preventiva. 
###### Justificativa: é funcional porque é uma ação de criação de registro realizada por um ator específico, o técnico. 

##### RF18 – O sistema deve alterar automaticamente o status do equipamento para "em manutenção" quando uma Ordem de Serviço for aberta para ele.  
###### Justificativa: é funcional porque descreve uma mudança de estado do sistema decorrente de uma ação, e essa mudança pode ser observada e testada. 

##### RF19 – O sistema deve gerar um alerta de manutenção preventiva quando o horímetro do equipamento atingir o limite configurado.  
###### Justificativa: é funcional porque "gerar um alerta" é uma ação concreta e visível do sistema, disparada por uma condição de negócio. 

##### RF20 – O técnico deve conseguir registrar o encerramento de uma Ordem de Serviço, informando peças utilizadas, mão de obra e custo total do serviço.  
###### Justificativa: é funcional porque é uma ação de registro de dados, executada por um ator específico, o técnico. 

##### RF21 – O administrador deve conseguir visualizar, no dashboard, indicadores de equipamentos disponíveis, alugados e em manutenção em tempo real.  
###### Justificativa: é funcional porque "visualizar indicadores" é uma ação que o usuário vê acontecer na tela, mesmo que os dados sejam agregados. 

##### RF22 – O sistema deve exibir, no dashboard, um ranking dos equipamentos mais utilizados e das obras com maior volume de locações. 
###### Justificativa: é funcional porque "exibir um ranking" é um comportamento concreto e testável do sistema, resultado de um processamento de dados. 

##### RF23 – O administrador deve conseguir gerar relatórios de utilização de equipamentos e de custos de manutenção por período.  
###### Justificativa: é funcional porque "gerar relatórios" é uma ação disparada pelo usuário e executada pelo sistema. 

##### RF24 – O administrador deve conseguir configurar os valores de tarifa de locação, sendo eles diária, semanal, quinzenal e mensal, para cada equipamento.  
###### Justificativa: é funcional porque "configurar valores" é uma ação de cadastro/edição de dados, e não uma característica de qualidade do sistema. 

##### RF25 – O usuário deve conseguir consultar, em seu perfil, o histórico completo de empréstimos e agendamentos já realizados.
###### Justificativa: é funcional porque a consulta de um histórico é uma ação visível e testável executada pelo usuário. 

### Requisitos Não Funcionais 

##### Os requisitos não funcionais descrevem as condições de qualidade, segurança, desempenho e usabilidade que o sistema deve atender enquanto executa as funções descritas na seção anterior. Após cada requisito, apresenta-se a justificativa de sua classificação. 

##### RNF01 – O sistema deve armazenar as senhas dos usuários de forma criptografada, nunca em texto puro. 
###### Justificativa: é não funcional porque não descreve uma ação visível ao usuário, mas sim uma propriedade de segurança que deve valer para o sistema inteiro, e que só é percebida quando falha. 

##### RNF02 – O sistema deve impedir o acesso de usuários não autenticados às páginas da área administrativa.  
###### Justificativa: é não funcional porque trata de uma restrição de segurança transversal a todo o sistema, e não de uma ação isolada de um módulo específico. 

##### RNF03 – O sistema deve carregar o catálogo de equipamentos e o dashboard em até três segundos em condições normais de rede.  
###### Justificativa: é não funcional porque estabelece uma condição de desempenho (tempo de resposta), e não uma ação que o sistema realiza. 

##### RNF04 – O sistema deve ser responsivo, permitindo que operadores registrem retiradas e devoluções corretamente a partir de celulares e tablets no canteiro de obra. 
###### Justificativa: é não funcional porque descreve uma característica de usabilidade e compatibilidade de interface, aplicável a todas as telas, e não uma ação específica. 

##### RNF05 – O sistema deve manter um registro de auditoria de todas as alterações de status dos equipamentos, com data, hora e usuário responsável. 
###### Justificativa: é não funcional porque trata de uma garantia de rastreabilidade e confiabilidade que perpassa todas as funcionalidades do sistema, e não de uma única ação. 

##### RNF06 – O sistema deve estar disponível para consulta e registro de operações em pelo menos 99% do tempo mensal.  
###### Justificativa: é não funcional porque define uma métrica de disponibilidade do sistema como um todo, e não uma ação executável por um usuário. 

##### RNF07 – A interface deve seguir um padrão visual consistente entre a área pública, a área do usuário e a área administrativa. 
###### Justificativa: é não funcional porque descreve uma característica de usabilidade e consistência visual, perceptível apenas quando ausente, e não uma ação do sistema. 

##### RNF08 – O sistema deve funcionar corretamente nos navegadores Google Chrome, Firefox e Edge em suas versões mais recentes. 
###### Justificativa: é não funcional porque é uma restrição técnica de compatibilidade, e não um comportamento ou ação do sistema. 

##### RNF09 – O sistema deve realizar backup automático diário da base de dados de equipamentos, contratos e manutenções. 
###### Justificativa: é não funcional porque, apesar de "realizar backup" parecer uma ação, trata-se de uma condição de confiabilidade e segurança dos dados que ocorre em segundo plano, sem interação do usuário, e é percebida apenas em caso de falha. 

##### RNF10 – O sistema deve suportar o cadastro de pelo menos 5.000 equipamentos e 500 usuários simultâneos sem perda perceptível de desempenho. 
###### Justificativa: é não funcional porque define um limite de escalabilidade e desempenho do sistema, e não uma ação executada por um usuário. 

##### Este levantamento reúne 25 requisitos funcionais e 10 requisitos não funcionais, cobrindo os módulos de login, usuários, categorias, equipamentos, agendamentos, empréstimos, devoluções, manutenções, dashboard e administração. Cada requisito foi redigido de forma específica e testável, e acompanhado de uma justificativa que explica por que ele pertence ao grupo funcional ou não funcional, de modo que seja possível verificar, durante a fase de validação, se o sistema o atende ou não. Os requisitos aqui apresentados servem de base para a modelagem do banco de dados, a definição das telas e o planejamento das próximas etapas de desenvolvimento do sistema Devisate Construções. 
