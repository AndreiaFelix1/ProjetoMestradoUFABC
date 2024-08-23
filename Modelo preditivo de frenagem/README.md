# Exemplo de modelo de predição

Nesse repositória está passo a passo de um modelo preditivo onde prevemos a posição futura de um veículo.

## 🚀 Cenário

Construção do cenário:

1. Na pasta Criação do cenário está os arquivos para criar o ambiente de treinamento e teste no sumo. 

2. O cenário de treinamento consiste em uma via reta de 1000 metros, onde em 500 metros há um semáforo que fica aberto por 35 segundos, depois fecha por 5 segundos, e permanece assim até finalizar a simulação, conforme imagem abaixo:

![Cenário Gerado no SUMO](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Modelo%20preditivo%20de%20frenagem/Cria%C3%A7%C3%A3o%20do%20cen%C3%A1rio/Cenario%20treinamento.png)

3. O cenário de teste consiste em uma via de 1000 metros, onde em 700 metros há um semáforo que fica aberto por 35 segundos, depois fecha por 5 segundos, e permanece assim até finalizar a simulação, conforme imagem abaixo:

![Cenário Gerado no SUMO](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Modelo%20preditivo%20de%20frenagem/Cria%C3%A7%C3%A3o%20do%20cen%C3%A1rio/Cenario%20teste.png)

4. É colocado 5 veículos para essa simulação percorrendo a simulação em linha reta.

## 🚀 Puxando dados do veins

1. No simulador veins é feito conforme código na pasta Modelos de Predição, e é printado na tela como mostra abaixo:

![Cenário Gerado no SUMO](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Modelo%20preditivo%20de%20frenagem/Modelos%20de%20predi%C3%A7%C3%A3o/teste2veins.png)

2. Os dados são colocados em um arquivo xlsx e é feito tratamento dos dados para evitar string no código.










