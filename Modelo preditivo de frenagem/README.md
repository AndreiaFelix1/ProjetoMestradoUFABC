# Exemplo de modelo de predição

Nesse repositória está exemplos de técnicas de predição para prever a posição futura de um veículo em um ambiente controlado. Todos os códigos usados para criar os cenários de simulação estão na pasta Criação do cenário.

## 🚀 Cenário

Para começar com este projeto, siga os passos abaixo:

1. Instale o simulador de mobilidade urbana SUMO no site oficial, versão 1.8 ou superior.

2. Crie na pasta bin do SUMO um arquivo com a extensão nod.xml como no arquivo de exemplo freewayandreia.nod.xml.

3. Crie na pasta bin do SUMO um arquivo com a extensão edg.xml como no arquivo de exemplo freewayandreia.edg.xml.

4. Crie na pasta bin do SUMO um arquivo de extensão netc.cfg como no arquivo meu.netc.cfg.

4. Arraste o arquivo netc.cfg para netconvert, será gerado um arquivo de rede com a extensão net.xml.

5. Para visualizar a rede criada abre o arquivo sumo-gui com duplo clique, clique em file -> open network -> selecione o arquivo de rede criado.

## 📷 Imagem de Exemplo

Aqui está uma imagem de exemplo da rede gerada em real world:

![Cenário Gerado no SUMO](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Exemplo%20de%20modelo%20preditivo%20de%20posi%C3%A7%C3%A3o%20de%201%20carro/Cria%C3%A7%C3%A3o%20do%20cen%C3%A1rio/Cen%C3%A1rio%20gerado%20no%20SUMO.png)

## 🚀 Criando tráfego

Para criar o tráfego com 20 veículos percorrendo a via:

1. Crie na pasta bin do SUMO um arquivo com a extensão nod.xml como no arquivo de exemplo freewayandreia.trips.xml.

2. Abra um terminal na pasta bin e adicione o código:

    ```bash
    duarouter --net-file C:\bin\freewayandreia.net.xml --route-files freewayandreia.trips.xml --output-file freewayandreia.rou.xml
    ```

3. Crie um arquivo de configuração com a extensão .sumocfg:

```python
    <configuration>
  <input>
    <net-file value="freewayandreia.net.xml"/>
    <route-files value="freewayandreia.rou.xml"/>
  </input>
</configuration>
```

4. Para visualizar a rede criada abre o arquivo sumo-gui com duplo clique, clique em file -> open simulation -> selecione o arquivo de simulação criado sumo.cfg.

## 📷 Imagem de Exemplo

Aqui está uma imagem de exemplo da simulação gerada em real world:

![Cenário Gerado no SUMO](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Exemplo%20de%20modelo%20preditivo%20de%20posi%C3%A7%C3%A3o%20de%201%20carro/Cria%C3%A7%C3%A3o%20do%20cen%C3%A1rio/Cen%C3%A1rio%20com%20carrinhos.png)

## 🚀 Treinamento e teste do modelo de predição

Para colocar a simulação no veins, printar na tela ID, posição e velocidade de um veículo, e treinar modelos de predição:

1. Os códigos está na pasta Criação do cenário.

2. Rode a simulação, a tela obtida será:

![Cenário Gerado no VEINS](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Exemplo%20de%20modelo%20preditivo%20de%20posi%C3%A7%C3%A3o%20de%201%20carro/Cria%C3%A7%C3%A3o%20do%20cen%C3%A1rio/Screenshot%20from%202024-08-23%2018-20-38.png)

2. Copie as informações obtidas no terminal e cole em um excel.

3. Foi feito uma plotagem de gráfico Velocidade x Tempo conforme abaixo:

![Cenário Gerado no colab](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Exemplo%20de%20modelo%20preditivo%20de%20posi%C3%A7%C3%A3o%20de%201%20carro/Modelos%20de%20predi%C3%A7%C3%A3o/Grafico%20velocidade%20x%20tempo.png)

4. Faça a limpeza dos dados, deixando apenas os primeiros números da posição e da velocidade.

5. Faça o treinamento nos modelos ARIMA, KNNregressor, regressão linear e SVR conforme a pasta Modelos de predição. A matriz de confusão dos nossos dados é:

![Cenário Gerado no colab](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Exemplo%20de%20modelo%20preditivo%20de%20posi%C3%A7%C3%A3o%20de%201%20carro/Modelos%20de%20predi%C3%A7%C3%A3o/Captura%20de%20tela%202024-08-23%20161108.png)

6. Os resultados da simulação obtidos são:

![Cenário Gerado no colab](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Exemplo%20de%20modelo%20preditivo%20de%20posi%C3%A7%C3%A3o%20de%201%20carro/Modelos%20de%20predi%C3%A7%C3%A3o/ResultadosSimulacoes.png)











## Referências

https://www.galirows.com.br/meublog/blog/introducao-ao-sumo/





