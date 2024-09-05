# Checkpoint 04 - O Caso da Vinheria Agnello
<img src="/img/circuito.png">

## Sensor de Luminosidade com ESP32 DevKit v1 e FIWARE

Este projeto implementa um **sensor de luminosidade** utilizando o **ESP32 DevKit v1** na plataforma **Wokwi**. O sistema realiza uma média de 10 leituras consecutivas da luminosidade do ambiente por meio de um **fotoresistor (LDR)**, enviando os dados para um broker **MQTT**. O projeto faz parte de uma solução mais ampla de monitoramento global de vinherias utilizando a plataforma **FIWARE**.

### Objetivo

O objetivo deste projeto é monitorar a luminosidade em vinherias de forma remota, integrando o sensor ao ecossistema FIWARE para envio de dados e gerenciamento via **API Postman**. O sensor ESP32 coleta dados e os envia para um broker MQTT, de onde o FIWARE Helix pode monitorar e tomar ações baseadas nas leituras.


### Acesso ao prototipo simulado
<a href="https://wokwi.com/projects/408016150371922945" target="_blank" style="text-align: center; margin-right: 10px;">
  <img loading="lazy" src="/img/wokwi.png" width="150px">
</a>

### Vídeo explicativo sobre o prejeto

<a href="https://www.youtube.com/watch?v=J-tl1dWq988" target="_blank" style="text-align: center; margin-right: 10px;">
  <img loading="lazy" src="/img/youtube.png" width="150px">
</a>

### Componentes Utilizados

- **ESP32 DevKit v1**
- **Módulo Sensor Fotoresistor (LDR)**
- **Fios de Conexão**

### Integração com FIWARE

Este projeto utiliza a **Plataforma FIWARE** como back-end da solução, onde:
- O **Postman** é usado para testar e consumir a API.
- Uma **Máquina Virtual no Azure** é utilizada para hospedar o servidor FIWARE, que gerencia o envio e recebimento de dados de luminosidade.

### Funcionalidades

- **Leitura da Luminosidade**: O sensor LDR coleta 10 leituras consecutivas, calculando a média, e envia o valor ao broker MQTT.
- **Publicação MQTT**: Os valores de luminosidade são publicados em um broker MQTT, permitindo a integração com o FIWARE Helix.
- **Controle via MQTT**: O sistema também possui controle de um LED onboard via comandos recebidos no MQTT.
  
### Passo a Passo de Reproduzir o Projeto

Para reproduzir este projeto, siga as instruções detalhadas no repositório do professor [Fábio Cabrini](https://github.com/fabiocabrini/fiware), que descreve como configurar o ambiente FIWARE e integrar dispositivos IoT com o broker MQTT e o Helix.

### Bibliotecas Utilizadas

As seguintes bibliotecas são necessárias para o funcionamento do código:

- **WiFi.h**: Para conexão com redes Wi-Fi.
- **PubSubClient.h**: Para comunicação com o broker MQTT.

### Plataforma

O desenvolvimento foi realizado na plataforma Wokwi, que permite simular a operação do ESP32 com o sensor LDR.

### Como Usar

Clone o repositório:

1. ```git clone https://github.com/seu-usuario/nome-do-repositorio.git```
2. Configure o ambiente FIWARE conforme as instruções no repositório do professor Cabrini.
3. Configure o código com as credenciais corretas de Wi-Fi e MQTT.
4. Faça o upload do código no ESP32 através da plataforma Wokwi ou Arduino IDE.
5. Monitore os dados de luminosidade e o estado do LED pelo Serial Monitor ou broker MQTT.

### Autores

<div style="display: flex; justify-content: space-between; align-items: center;">
<a href="https://github.com/jaoAprendiz" target="_blank" style="text-align: center; margin-right: 10px;">
<img loading="lazy" src="https://avatars.githubusercontent.com/jaoAprendiz" width=120>
<p style="font-size:min(2vh, 36px); margin-top: 10px;">João Victor - RM 557595</p>
</a>

<a href="https://github.com/K1rit03" target="_blank" style="text-align: center; margin-right: 10px;">
<img loading="lazy" src="https://avatars.githubusercontent.com/K1rit03" width=120>
<p style="font-size:min(2vh, 36px); margin-top: 10px;">Thiago Oliveira - RM 555485</p>
</a>
</div>

<a href="https://github.com/JeannMatheuss" target="_blank" style="text-align: center; margin-right: 10px;">
<img loading="lazy" src="https://avatars.githubusercontent.com/JeannMatheuss" width=120>
<p style="font-size:min(2vh, 36px); margin-top: 10px;">Jean Matheus - RM 555519</p>
</a>


<a href="https://github.com/Malice112" target="_blank" style="text-align: center; margin-right: 10px;">
<img loading="lazy" src="https://avatars.githubusercontent.com/Malice112" width=120>
<p style="font-size:min(2vh, 36px); margin-top: 10px;">Maria Alice - 557516</p>
</a>


<a href="https://github.com/iannyrfs" target="_blank" style="text-align: center; margin-right: 10px;">
<img loading="lazy" src="https://github.com/iannyrfs" width=120>
<p style="font-size:min(2vh, 36px); margin-top: 10px;">Ianny Raquel - 559096</p>
</a>
</div>

### Licença

Este projeto está licenciado sob a licença MIT.
