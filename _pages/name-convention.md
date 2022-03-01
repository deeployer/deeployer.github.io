[Home](https://deeployer.com/deeployer-patterns-and-practices/) > Name Convention

# Name Convention

Neste paper encontram-se as convenções de nomenclatura para criação de projetos no Visual Studio (Code), recursos na Azure, itens no Azure DevOps etc.

**Motivação**

Seguir um conjunto consistente de convenções de nomenclatura no desenvolvimento pode ser uma grande contribuição para a usabilidade de uma estrutura.

Os padrões permitem que a estrutura seja usada por muitos desenvolvedores em projetos e equipes separadas. Além da consistência da forma, os nomes dos elementos devem ser facilmente compreendidos e devem transmitir inequivocamente sua função/propósito. 

**Regras gerais**

- Utilizar sempre nomes com letras minúsculas, os temos entre "<>" estão utilizando Pascal Case apenas para legibilidade;
- Termos que não estiverem entre "<>" são fixos e obrigatórios no nome;
- Não utilizar abreviações, que muitas vezes podem gerar confusões no entendimento;
- Não utilizar acrônimos, a menos que sejam amplamente reconhecidos e aceitos.

## Azure

### Resource Group

- **Name convention:** ```<Environment>-<Region>-<BusinessUnitName>-<ProductName>-<Purpose>```
- **Exemplo de uso:** dev-br-deephealth-data-ingest

### Azure Storage Account

- **Name convention:** ```<BusinessUnitName>-<ProductName>-<Purpose>```
- **Exemplo de uso:** deephealthprocess
- **Exemplo de uso:** deephealthdata

### Azure Storage Account - Queue

- **Name convention:** ```<StorageAccountName>-<Purpose>-in```
- **Name convention:** ```<StorageAccountName>-<Purpose>-in-poison```
- **Exemplo de uso:** deephealth-process-download-in
- **Exemplo de uso:** deephealth-process-download-in-poison

### Azure Storage Account - Container

- **Name convention:** seguir a segregação lógica necessária para representar seu propósito.

### Azure SQL Server - Database 

- **Name convention:** ```<BusinessUnit>-target```
- **Name convention:** ```<BusinessUnit>-stage```

### Azure SQL Server - Schema

- **Name convention:** ```<CollectionName>```
- **Exemplo de uso:** cnes

### Azure SQL Server - Table

- **Name convention:** ```<Schema>.<SourceTableName>```
- **Exemplo de uso:** sia-tb-ap-aq

## Projetos desenvolvidos no Visual Studio (Code)

### Projeto para uma Azure Functions

- **Name convention:** ```<BusinessUnitName>-<ProductName>-func-<Purpose>```
- **Exemplo de uso:** deephealth-data-func-ftp-scan
- **Exemplo de uso:** deephealth-data-func-ftp-download

## Azure DevOps

To-do

## Atlas / MongoDB

### NoSQL database name

- **Name convention:** ```<BusinessUnitName>-<ProductName>-<Purpose>```
- **Exemplo de uso:** deephealth-data-ftp-scan-ingest--control

### NoSQL database collection name

- **Name convention:** ```<SourceName>-<ItemName>```
- **Exemplo de uso:** datasus-cnes

<p align="center">
  <img width="200" height="200" src="https://deeployer.com/deeployer-patterns-and-practices/assets/images/deeployer-logo-hexagon-avatar.png">
</p>
