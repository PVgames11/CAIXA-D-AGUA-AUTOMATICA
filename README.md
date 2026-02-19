# Sistema Inteligente de Monitoramento e Controle de Caixa d’Água com ESP32
Visão Geral

Este projeto apresenta o desenvolvimento de um sistema inteligente de monitoramento e controle de caixa d’água, baseado na plataforma ESP32, com medição de nível por sensor ultrassônico e acionamento automático de bomba através de relé.

A solução permite acompanhar, em tempo real, o nível de água da caixa, visualizar o volume disponível por meio de uma interface web embarcada e realizar o controle automático ou manual da bomba, garantindo maior eficiência operacional e segurança no abastecimento.

# Arquitetura do Sistema

O sistema é composto pelos seguintes elementos:

ESP32 como unidade central de processamento e comunicação

Sensor ultrassônico para medição do nível de água

Módulo relé para acionamento da bomba

Interface web hospedada diretamente no ESP32

Comunicação via rede Wi-Fi local

Atualmente, o acesso à interface web é restrito a dispositivos conectados à mesma rede Wi-Fi da ESP32, utilizando o endereço IP local atribuído ao microcontrolador.

# Funcionalidades

Medição contínua do nível de água da caixa

Cálculo automático do volume em litros e percentual de preenchimento

Controle automático da bomba de acordo com regras predefinidas:

Acionamento automático quando o nível é igual ou inferior a 15%

Desligamento automático quando o nível atinge ou ultrapassa 90%

Modo de manutenção para bloqueio completo do acionamento da bomba

Interface web responsiva com:

Exibição do nível da água

Barra de progresso visual

Indicação do estado da bomba

Controles manuais para ligar e desligar a bomba

# Lógica de Controle

O sensor ultrassônico realiza a leitura da distância até a superfície da água. A partir dessa medida, o sistema calcula a altura da lâmina de água, o volume total presente na caixa e o percentual de ocupação.

Com base nesses dados, a bomba é controlada automaticamente, respeitando os limites mínimos e máximos definidos. O modo de manutenção, quando ativado, tem prioridade sobre qualquer outro comando, garantindo que a bomba permaneça desligada independentemente do nível da água.

# Tecnologias Utilizadas

ESP32

Sensor ultrassônico

Módulo relé

Linguagem C/C++

Wi-Fi (WebServer embarcado)

HTML e CSS para interface web

# Acesso ao Sistema

O sistema pode ser acessado através de um navegador web, utilizando o endereço IP local da ESP32.

Observação:
Nesta versão, o acesso é restrito à rede local. Dispositivos externos ou redes diferentes não conseguem acessar a interface.

# Evolução do Projeto

Este projeto foi desenvolvido com foco em escalabilidade e evolução tecnológica. As próximas etapas previstas incluem:

Integração com protocolo MQTT para comunicação em tempo real

Integração com Firebase para armazenamento de dados e acesso remoto

Possibilidade de monitoramento e controle da caixa d’água de qualquer local com acesso à internet

Implementação de autenticação e controle de usuários

Essas melhorias transformarão o sistema em uma solução completa de Internet das Coisas (IoT).

# Aplicações

Residências

Condomínios

Escolas

Pequenos comércios

Projetos educacionais e acadêmicos

Estudos de automação e IoT

# Autor

Paulo Vitor Silva Quintanilha
Bacharel em Ciência da Computação
Área de atuação: Automação, Robótica, Internet das Coisas e Sistemas Inteligentes

# Licença

Este projeto é de livre uso para fins educacionais e experimentais. Ajustes e expansões podem ser realizados conforme a necessidade do usuário.
