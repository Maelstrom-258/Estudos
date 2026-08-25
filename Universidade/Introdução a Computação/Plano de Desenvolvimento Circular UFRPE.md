# Rascunho
Elabore um plano de desenvolvimento para o app chamado CircuMobi:
O aplicativo possui dois níveis de atuação, uma para usuários motoristas e a outra, por padrão ao usá-lo, de passageiro. 
## Interface Motorista
Objetivo: Servir como ponta de input da latitude e longitude, para definir onde o ônibus circular está, usado na interface do passag
eiro.
Funcionalidades: Principalmente transmissão da localização do circular em intervalo padrão de 10 segundos, visando otimização do sistema para o motorista.
dados de entrada: Latitude e Longitude partindo do celular do motorista
Plataforma pretendida: Mobile (Aplicativo de celular, acessível para ambos android e apple.)
restrições ou preferências: O aplicativo vai ter algumas opções de funcionamento partindo da ponta do motorista, se deseja usar um intervalo menor ou maior (limite 30s) e definir seu horário de almoço e de inatividade, o qual automaticamente vai parar o funcionamento do aplicativo toda vez que ocorrer. O motorista também pode definir a capacidade do circular, por padrão (quantia de passageiros do circular)

********
## Interface Passageiro
Objetivo: Mostrar, no mapa, a localização atual do ônibus circular, além disso, mostrar as paradas usuais do ônibus, se ele está parado ou não, e horário estimado para chegada em determinadas paradas.
Funcionalidades: Localização do circular em tempo real; visualização, no mapa, de paradas do ônibus; Ver quando o circular está ou não funcionando; além de poder servir como contador de pessoas no ônibus para saber a lotação.
Dados de entrada: Localização do celular do passageiro para observação no mapa de parada mais próxima e horário.
Plataforma pretendida: Mobile (Aplicativo de celular, acessível para ambos android e apple.)
Restrições ou preferências: A localização do celular, quando próxima aos pontos de tick do próprio motorista vai servir para denotar um passageiro dentro do ônibus. 

********
## Formato de resposta esperado: 
Elaboração de etapas para o planejamento do aplicativo, lista de tecnologias para implementar a interface do motorista assim como frameworks que serão utilizados no desenvolvimento. Estabelecimento de um fluxo de dados baseado em administração (Planejamento -> Organização -> Desenvolvimento -> Controle) onde controle será uma etapa de testes para eliminar erros e quaisquer problemas que serão encontrados.


# Prompt Final 1

Elabore um plano de desenvolvimento para o app CircuMobi, um aplicativo mobile destinado ao rastreamento e acompanhamento dos ônibus circulares da UFRPE. O sistema deve possuir duas interfaces principais: uma interface destinada aos motoristas, responsável pelo envio dos dados de localização do ônibus, e uma aos passageiros, que utilizará esses dados para acompanhar o circular, visualizar suas paradas e estimar sua chegada.
## Interface do motorista

A interface do motorista terá como principal objetivo funcionar como a **fonte dos dados de localização do ônibus**, utilizando o GPS do celular do motorista para transmitir a latitude e a longitude atuais do veículo para o sistema (Ver fluxograma).

A localização deverá ser enviada por padrão em um intervalo de 10 segundos, buscando equilibrar precisão da localização, consumo de bateria, uso de dados móveis e desempenho do sistema. O motorista deverá possuir algumas opções de configuração do funcionamento do rastreamento, incluindo:
- Definir o intervalo de atualização da localização, podendo utilizar um intervalo menor ou maior que o padrão de 10 segundos, respeitando um limite máximo de 30 segundos.
- Definir seu horário de almoço, fazendo com que o sistema suspenda automaticamente a transmissão da localização durante esse período.
- Definir períodos de inatividade, durante os quais o envio da localização deverá ser interrompido automaticamente.
- Informar a capacidade máxima de passageiros do ônibus circular.

Os dados principais fornecidos por essa interface serão **latitude**, **longitude**, **horário da atualização**, **identificação do ônibus/motorista** e através do cálculo entre uma localização e outra, se o ônibus **está andando ou não**.
## Interface do passageiro

A interface do passageiro deverá permitir acompanhar o circular de maneira visual e suas principais funcionalidades deverão incluir:
- Exibir no mapa a **localização atual do ônibus em tempo real.**
- Exibir as **paradas usuais do circular** no mapa.
- Informar se o ônibus está atualmente em **circulação, parado, em intervalo ou inativo**.
- Calcular e apresentar uma **estimativa do horário de chegada do ônibus às próximas paradas**.
- Permitir que o passageiro identifique a parada mais próxima utilizando a localização do próprio celular.
- Exibir uma **estimativa da lotação atual** do ônibus.

%%Para a estimativa de lotação, considere como hipótese que a localização do celular dos passageiros, quando estiver próxima dos últimos "Ticks" de localização do motorista, possa ser utilizada para inferir a quantia de passageiros no ônibus.%%
## Dados e funcionamento do sistema (Infraestrutura)

Considere que o aplicativo precisará possuir uma infraestrutura responsável por receber, armazenar, processar e distribuir os dados enviados pelos celulares dos motoristas para os passageiros.

Descreva como deverá funcionar o fluxo de dados entre:

Celular do motorista;
Servidor ou serviço de backend;
Banco de dados;
Sistema de mapas e cálculo de localização/rota;
Celular do passageiro.

Explique também quais dados devem ser armazenados, quais dados devem ser transmitidos em tempo real e quais informações podem ser calculadas sob demanda.

## Plataformas

O aplicativo deverá ser desenvolvido para dispositivos móveis, com suporte tanto para Android quanto para iOS. Priorize uma arquitetura que permita **compartilhar o máximo possível do código** entre as duas plataformas, reduzindo custos e complexidade de desenvolvimento.
## Requisitos e restrições

Considere os seguintes requisitos:
- O rastreamento deve funcionar de **maneira adequada em segundo plano quando necessário**.
- O sistema deve procurar **minimizar o consumo de bateria** e de **internet móvel** do celular do motorista.
- A localização deve possuir atualização suficientemente frequente para permitir acompanhamento em tempo real.
- O sistema **deve continuar funcionando de maneira segura mesmo em situações de instabilidade ou perda temporária de conexão**.
- O sistema deve possuir **autenticação adequada para diferenciar motoristas de passageiros**.
- A interface do motorista deverá **exigir autenticação ou algum mecanismo de autorização**.
- O sistema deverá considerar segurança e privacidade dos dados de localização dos usuários.
- O projeto deve ser suficientemente simples para servir como uma primeira versão funcional do sistema, mas deve permitir evolução futura.
- Considere acessibilidade, facilidade de uso e clareza da interface como requisitos importantes.

********
## Planejamento administrativo e fluxo de desenvolvimento

Organize o desenvolvimento utilizando quatro etapas principais:
### Planejamento

Defina o problema, objetivos, requisitos funcionais e não funcionais, usuários, arquitetura inicial, riscos e prioridades do projeto.
### Organização

Defina a divisão das funcionalidades, componentes do sistema, tecnologias necessárias, estrutura do banco de dados, organização da equipe e **sequência de implementação**.
### Desenvolvimento

Apresente as etapas de implementação do aplicativo, incluindo desenvolvimento da interface do motorista, interface do passageiro, backend, banco de dados, comunicação em tempo real, integração com mapas, autenticação e sistema de estimativa de chegada e lotação.
### Controle

Defina como o sistema deverá ser testado e validado. Inclua testes funcionais, testes de localização, testes de comunicação em tempo real, testes de desempenho, consumo de bateria, conectividade instável, segurança, privacidade e testes das estimativas de chegada e lotação. Indique também como erros encontrados deverão ser identificados, corrigidos e posteriormente testados novamente.

## Tecnologias

Apresente uma lista das tecnologias, linguagens, frameworks, bibliotecas, serviços e ferramentas recomendadas para implementar o projeto.

Justifique brevemente a escolha de cada tecnologia, especialmente para:
- Desenvolvimento mobile multiplataforma;
- GPS e localização em segundo plano;
- Backend;
- Banco de dados;
- Comunicação em tempo real;
- Autenticação;
- Mapas;
- Cálculo de rotas e estimativa de chegada;
- Hospedagem e infraestrutura;
- Monitoramento e testes.

Apresente também pelo menos uma alternativa tecnológica relevante para os principais componentes e compare suas vantagens e desvantagens.


# Prompt final 2
## Plano de Desenvolvimento do Aplicativo CircuMobi

Elabore um plano de desenvolvimento para o app CircuMobi, um aplicativo mobile destinado ao rastreamento e acompanhamento dos ônibus circulares da UFRPE. O sistema precisa ter duas interfaces principais: uma para os motoristas, que enviará os dados de localização do ônibus, e outra para os passageiros, que usará esses dados para acompanhar o ônibus, ver suas paradas e saber a hora de chegada.

## Interface do Motorista

A interface do motorista serve como a fonte dos dados de localização do ônibus. Ela usará o GPS do celular do motorista para enviar a latitude e a longitude do veículo para o sistema. O sistema precisa enviar esses dados a cada 10 segundos, para equilibrar precisão, bateria, dados móveis e desempenho. O motorista pode ajustar o intervalo de envio, mas não pode exceder 30 segundos. Além disso, o motorista pode definir horário de almoço, para que o sistema pare de enviar dados durante esse período, e pode definir períodos de inatividade, onde o envio também para. O motorista também precisa informar a capacidade máxima do ônibus.

Os dados principais coletados pela interface do motorista são latitude, longitude, horário da atualização, identificação do ônibus e do motorista, e se o ônibus está andando ou parado.

## Interface do Passageiro

A interface do passageiro permite acompanhar o ônibus de forma visual. Suas principais funcionalidades incluem exibir a localização em tempo real no mapa, mostrar as paradas usuais, informar o estado atual do ônibus (em circulação, parado, em intervalo ou inativo), calcular a estimativa de chegada às próximas paradas, identificar a parada mais próxima com base na localização do celular e mostrar a lotação atual do ônibus.

Para estimar a lotação, o sistema pode usar a localização dos passageiros, se eles estiverem perto dos últimos dados de localização do motorista.

## Dados e Funcionamento do Sistema

O sistema precisa ter uma infraestrutura para receber, armazenar, processar e distribuir os dados dos motoristas para os passageiros. O fluxo de dados deve seguir os seguintes passos:

Celular do motorista → Servidor ou serviço de backend → Banco de dados → Sistema de mapas e cálculo → Celular do passageiro.

O sistema precisa armazenar dados como latitude, longitude, horário, identificação do ônibus e status. Dados em tempo real incluem localização atual do ônibus. Informações como lotação e chegada podem ser calculadas sob demanda.

## Plataformas

O aplicativo será desenvolvido para Android e iOS. A arquitetura deve permitir compartilhar o máximo de código entre as duas plataformas, para reduzir custos e complexidade.

## Requisitos e Restrições

O sistema precisa funcionar em segundo plano, minimizar o uso de bateria e internet, ter atualizações frequentes para acompanhar de forma em tempo real, funcionar mesmo em conexões instáveis, ter autenticação segura para motoristas e passageiros, e seguir normas de segurança e privacidade. O projeto precisa ser simples, mas permitir evolução futura. Acessibilidade e clareza da interface são importantes.

## Planejamento Administrativo e Fluxo de Desenvolvimento

O desenvolvimento será dividido em quatro etapas principais:

### Planejamento

Definir o problema, os objetivos, os requisitos funcionais e não funcionais, os usuários, a arquitetura inicial, os riscos e as prioridades do projeto.

### Organização

Dividir as funcionalidades, os componentes do sistema, as tecnologias necessárias, a estrutura do banco de dados, a organização da equipe e a sequência de implementação.

### Desenvolvimento

Implementar as interfaces do motorista e do passageiro, o backend, o banco de dados, a comunicação em tempo real, a integração com mapas, a autenticação e o sistema de estimativa de chegada e lotação.

### Controle

Definir como o sistema será testado, incluindo testes funcionais, de localização, de comunicação em tempo real, de desempenho, de bateria, de conectividade instável, de segurança, privacidade, e de estimativas. Mostrar como os erros serão identificados, corrigidos e testados novamente.

## Tecnologias

Listar as tecnologias, linguagens, frameworks, bibliotecas, serviços e ferramentas recomendadas para o projeto.

Justificar a escolha de cada tecnologia, especialmente para:

- Desenvolvimento mobile multiplataforma;
- GPS e localização em segundo plano;
- Backend;
- Banco de dados;
- Comunicação em tempo real;
- Autenticação;
- Mapas;
- Cálculo de rotas e estimativa de chegada;
- Hospedagem e infraestrutura;
- Monitoramento e testes.

Também apresentar alternativas para os principais componentes e comparar vantagens e desvantagens.