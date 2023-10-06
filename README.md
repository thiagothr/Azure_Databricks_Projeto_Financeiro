# Azure-Databricks-Analise-Bancario
Projeto de engenharia de dados envolvendo Microsoft Azure e Databricks para processamento de transições bancários

## Escopo do projeto 
Este projeto visa a cronstrução de toda a arquitetura, fluxo e processamento de dados de transições bancárias de um banco fictcio utilizando das mais diversas funções disponibilizadas pela cloud Azure e Linguagem Python.

## Arquitetura do projeto 
O projeto utiliza a arquitetura em nuvem da Microsoft Azure.O Azure oferece recursos e ferramentas para ajudar no desenvolvimento e implantação de aplicativos, além de garantir alta disponibilidade, segurança e desempenho.

![image](https://github.com/thiagothr/Azure-Databricks-Projeto-Bancario/assets/72639507/d0ec7b34-3196-4232-8be2-d5b0743be505)


Alguns dos serviços utilizados pra este projeto foram:
  - Azure Key Vault
  - Azure Storage Account(Data Lakes)
  - Azure Databricks Workspace
  - Python
  - Pyspark
  - SQL Database
  - Servidores SQL
  - Azure Active Directory
  - Power BI

Além do gerenciamento de assinaturas, recursos, permissões, regiões, urls, tokens, clusters, pipelines, dentre outros.

## Descrição do projeto
- Nesta seção vou destacar alguns passos e desafios ao decorrer deste projeto. O primeiro passo do projeto foi a importação de base de dados público do kaggle. Importamos dados com estrutura CSV e JSON para futuramente ser tratado em ambiente em nuvem.
- Após ser criada uma conta na plataforma da Azure, e tendo feito toda a criação de recursos e configurações de segurança na plataforma relacionados ao projeto, foi criado um Storage Account (Data Lake) de modo a simular uma situação real em que os CSV's estariam disponíveis para extração dessa estrutura de dados, e é neste local que que os dados extraídos do KAGGLE vão ser armazenados.

- Com arquivo enviado para o Storage Account e pronto para fazer todo o tratamento dessa estrutura conforme a imagem abaixo.

![image](https://github.com/thiagothr/Azure-Databricks-Projeto-Bancario/assets/72639507/196de851-eeb1-4b93-89c6-32b72e4d6c93)


- Nesta etapa são realizados a criação de scripts utilizando PySpark para fazer a conexão do Storage Account com o Databricks e leitura do dataset CSV e implementação de regras de negócio para processar os dados de forma precisa, para então realizar a conexão com o Azure SQL database disponibilizando os dados através de tabelas estruturadas para facilitar a disponibilização para quem utiliza de soluções de analises para como Power BI.

- O próximo passo é iniciar a realização da fase de processamento dos dados armazenados. E para isto, é criado um workspace no ## DATABRICKS.

![image](https://github.com/thiagothr/Azure-Databricks-Projeto-Bancario/assets/72639507/bce61935-3e7c-4d3b-8199-1f185ffb7d72)


- Na imagem acima é criado um cluster no Databricks com as configurações um pouco mais básicas pois a carga de processamento do nosso projeto não precisa de maiores configurações.

- Nesta etapa são realizados a criação de scripts utilizando PySpark como conexão do Storage Account com o Databricks e leitura do dataset CSV e implementação de regras de negócio para processar os dados de forma precisa para então realizar a conexão com o Azure SQL database disponibilizando os dados através de tabelas estruturadas para facilitar a disponibilização para quem utiliza de soluções de analises para como Power BI.

## mount entre azure storage account com o databricks

![image](https://github.com/thiagothr/Azure-Databricks-Projeto-Bancario/assets/72639507/a61b62ab-560b-4d9b-853a-51982c813e8b)

- Além do script criado foi também configurado e criado o SecretScope para armazenar usuário e senhas para fim de ter um segurança dentro da ferramenta


![image](https://github.com/thiagothr/Azure-Databricks-Projeto-Bancario/assets/72639507/a7b5aea7-80b2-4fd0-a66a-6fcc04dece2e)


## Filtragem dos clientes que tem o maior limite e que tiveram transições acima de 4000 reais
![image](https://github.com/thiagothr/Azure-Databricks-Projeto-Bancario/assets/72639507/90eb514f-a937-406e-b1c7-8c9ada2313e4)

## Conexão do Azure databricks com Azure SQL Database
![image](https://github.com/thiagothr/Azure-Databricks-Projeto-Bancario/assets/72639507/33cf6173-e470-438a-8e48-3da5e10e7402)

- Então após a criação de todo o script e conexão com o banco do Azure na imagem abaixo pode ver todo o dataset gerado no databricks estruturado no banco para então ser disponibilizado para analises e criações de dashboard.

![image](https://github.com/thiagothr/Azure-Databricks-Projeto-Bancario/assets/72639507/2fbd392a-420c-4c9b-8db2-82c0e315a3b2)



