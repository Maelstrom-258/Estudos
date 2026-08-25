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


# Prompt Final

Elabore um plano de desenvolvimento para o app CircuMobi, um aplicativo mobile destinado ao rastreamento e acompanhamento, em tempo real, dos ônibus circulares da UFRPE. O sistema deverá possuir duas interfaces principais: uma interface destinada aos motoristas, responsável pelo envio dos dados de localização e estado do ônibus, e uma interface destinada aos passageiros, que utilizará esses dados para acompanhar o circular, visualizar suas paradas e estimar sua chegada.
## 1. Interface do motorista

A interface do motorista terá como principal objetivo funcionar como a **fonte dos dados de localização do ônibus**, utilizando o GPS do celular do motorista para transmitir a latitude e a longitude atuais do veículo para o sistema (Ver fluxograma).

A localização deverá ser enviada inicialmente em um intervalo padrão de 10 segundos, buscando equilibrar precisão da localização, consumo de bateria, uso de dados móveis e desempenho do sistema.

O motorista deverá possuir algumas opções de configuração do funcionamento do rastreamento, incluindo:

- Definir o intervalo de atualização da localização, podendo utilizar um intervalo menor ou maior que o padrão de 10 segundos, respeitando um limite máximo de 30 segundos.
- Definir seu horário de almoço, fazendo com que o sistema suspenda automaticamente a transmissão da localização durante esse período.
- Definir períodos de inatividade, durante os quais o envio da localização deverá ser interrompido automaticamente.
- Informar a capacidade máxima de passageiros do ônibus circular.

Os dados principais fornecidos por essa interface serão latitude, longitude, horário da atualização, identificação do ônibus/motorista e estado de funcionamento do veículo.

## 2. Interface do passageiro

A interface do passageiro deverá permitir acompanhar o circular de maneira simples e visual.

Suas principais funcionalidades deverão incluir:

- Exibir no mapa a localização atual do ônibus em tempo real.
    
- Exibir as paradas usuais do circular no mapa.
    
- Informar se o ônibus está atualmente em circulação, parado, em intervalo ou inativo.
    
- Calcular e apresentar uma estimativa do horário de chegada do ônibus às próximas paradas.
    
- Permitir que o passageiro identifique a parada mais próxima utilizando a localização do próprio celular.
    
- Exibir uma estimativa da lotação atual do ônibus.
    
- Informar a capacidade máxima do circular e comparar essa capacidade com a quantidade estimada de passageiros.
    

Para a estimativa de lotação, considere como hipótese de funcionamento que a localização do celular dos passageiros, quando estiver próxima das paradas utilizadas como pontos de referência do sistema, possa ser utilizada para inferir a entrada ou saída de passageiros do ônibus. Analise essa abordagem e indique no plano possíveis limitações, riscos de privacidade, imprecisões e alternativas técnicas mais confiáveis.

## 3. Dados e funcionamento do sistema

Considere que o aplicativo precisará possuir uma infraestrutura responsável por receber, armazenar, processar e distribuir os dados enviados pelos celulares dos motoristas para os passageiros.

Descreva como deverá funcionar o fluxo de dados entre:

1. Celular do motorista;
    
2. Servidor ou serviço de backend;
    
3. Banco de dados;
    
4. Sistema de mapas e cálculo de localização/rota;
    
5. Celular do passageiro.
    

Explique também quais dados devem ser armazenados, quais dados devem ser transmitidos em tempo real e quais informações podem ser calculadas sob demanda.

## 4. Plataforma

O aplicativo deverá ser desenvolvido para dispositivos móveis, com suporte tanto para Android quanto para iOS.

Priorize uma arquitetura que permita compartilhar o máximo possível do código entre as duas plataformas, reduzindo custos e complexidade de desenvolvimento.

## 5. Requisitos e restrições

Considere os seguintes requisitos:

- O rastreamento deve funcionar de maneira adequada em segundo plano quando necessário.
    
- O sistema deve procurar minimizar o consumo de bateria e de internet móvel do celular do motorista.
    
- A localização deve possuir atualização suficientemente frequente para permitir acompanhamento em tempo real.
    
- O sistema deve continuar funcionando de maneira segura mesmo em situações de instabilidade ou perda temporária de conexão.
    
- O sistema deve possuir autenticação adequada para diferenciar motoristas de passageiros.
    
- Usuários passageiros devem utilizar a interface de passageiro por padrão.
    
- A interface do motorista deverá exigir autenticação ou algum mecanismo de autorização.
    
- O sistema deverá considerar segurança e privacidade dos dados de localização dos usuários.
    
- O projeto deve ser suficientemente simples para servir como uma primeira versão funcional do sistema, mas deve permitir evolução futura.
    
- Considere acessibilidade, facilidade de uso e clareza da interface como requisitos importantes.
    

## 6. Planejamento administrativo e fluxo de desenvolvimento

Organize o desenvolvimento utilizando quatro etapas principais:

### Planejamento

Defina o problema, objetivos, requisitos funcionais e não funcionais, usuários, arquitetura inicial, riscos e prioridades do projeto.

### Organização

Defina a divisão das funcionalidades, componentes do sistema, tecnologias necessárias, estrutura do banco de dados, organização da equipe e sequência de implementação.

### Desenvolvimento

Apresente as etapas de implementação do aplicativo, incluindo desenvolvimento da interface do motorista, interface do passageiro, backend, banco de dados, comunicação em tempo real, integração com mapas, autenticação e sistema de estimativa de chegada e lotação.

### Controle

Defina como o sistema deverá ser testado e validado. Inclua testes funcionais, testes de localização, testes de comunicação em tempo real, testes de desempenho, consumo de bateria, conectividade instável, segurança, privacidade e testes das estimativas de chegada e lotação. Indique também como erros encontrados deverão ser identificados, corrigidos e posteriormente testados novamente.

## 7. Tecnologias

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

## 8. Formato da resposta

Estruture a resposta como um plano de desenvolvimento técnico e administrativo do CircuMobi.

A resposta deverá conter, nesta ordem:

1. Resumo do projeto;
    
2. Problema que o aplicativo pretende resolver;
    
3. Perfis de usuários;
    
4. Requisitos funcionais;
    
5. Requisitos não funcionais;
    
6. Arquitetura geral do sistema;
    
7. Fluxo de dados entre motorista, servidor e passageiro;
    
8. Etapas de Planejamento, Organização, Desenvolvimento e Controle;
    
9. Tecnologias e frameworks recomendados;
    
10. Estrutura básica do banco de dados;
    
11. Principais riscos e desafios técnicos;
    
12. Estratégias de segurança e privacidade;
    
13. Estratégia de testes e validação;
    
14. Possível cronograma de desenvolvimento;
    
15. Sugestões para futuras versões do aplicativo.
    

Sempre que uma decisão técnica depender de uma hipótese não definida no enunciado, deixe a hipótese explícita e explique sua consequência para o projeto. Evite respostas genéricas e forneça informações suficientemente específicas para que uma equipe de desenvolvimento consiga transformar o plano em uma primeira versão funcional do aplicativo.