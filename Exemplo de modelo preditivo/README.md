# Exemplo de modelo de predição de posição

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

![Cenário Gerado no SUMO](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Exemplo%20de%20modelo%20preditivo/Cria%C3%A7%C3%A3o%20do%20cen%C3%A1rio/Cen%C3%A1rio%20gerado%20no%20SUMO.png)

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

![Cenário Gerado no SUMO](https://github.com/AndreiaFelix1/ProjetoMestradoUFABC/blob/main/Exemplo%20de%20modelo%20preditivo/Cria%C3%A7%C3%A3o%20do%20cen%C3%A1rio/Cen%C3%A1rio%20com%20carrinhos.png)




## Referências

https://www.galirows.com.br/meublog/blog/introducao-ao-sumo/



