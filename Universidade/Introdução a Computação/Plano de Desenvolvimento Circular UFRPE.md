Elabore um plano de desenvolvimento para o app chamado CircuMobi:
O aplicativo possui duas castas, uma para usuários motoristas e a outra, por padrão ao usá-lo, de passageiro. 
## Interface Motorista
Objetivo: Servir como ponta de input da latitude e longitude, para definir onde o ônibus circular está, usado na interface do passageiro.
Funcionalidades: Principalmente transmissão da localização do circular em intervalo padrão de 10 segundos, visando otimização do sistema para o motorista.
dados de entrada: Latitude e Longitude partindo do celular do motorista
Plataforma pretendida: Mobile (Aplicativo de celular, acessível para ambos android e apple.)
restrições ou preferências: O aplicativo vai ter algumas opções de funcionamento partindo da ponta do motorista, se deseja usar um intervalo menor ou maior (limite 30s) e definir seu horário de almoço e de inatividade, o qual automaticamente vai parar o funcionamento do aplicativo toda vez que ocorrer. O motorista também pode definir a capacidade do circular, por padrão (quantia de passageiros do circular)
## Interface Passageiro
Objetivo: Mostrar, no mapa, a localização atual do ônibus circular, além disso, mostrar as paradas usuais do ônibus, se ele está parado ou não, e horário estimado para chegada em determinadas paradas.
Funcionalidades: Localização do circular em tempo real; visualização, no mapa, de paradas do ônibus; Ver quando o circular está ou não funcionando; além de poder servir como contador de pessoas no ônibus para saber a lotação.
Dados de entrada: Localização do celular do passageiro para observação no mapa de parada mais próxima e horário.
Plataforma pretendida: Mobile (Aplicativo de celular, acessível para ambos android e apple.)
Restrições ou preferências: A localização do celular, quando próxima aos pontos de tick do próprio motorista vai servir para denotar um passageiro dentro do ônibus. 

## Formato de resposta esperado: 
Elaboração de etapas para o planejamento do aplicativo, lista de tecnologias para implementar a interface do motorista assim como frameworks que serão utilizados no desenvolvimento. Estabelecimento de um fluxo de dados baseado em administração (Planejamento -> Organização -> Desenvolvimento -> Controle) onde controle será uma etapa de testes para eliminar erros e quaisquer problemas que serão encontrados.