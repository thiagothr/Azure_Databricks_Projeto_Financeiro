# Azure-Databricks-Analise-Bancario
Projeto de engenharia de dados envolvendo Microsoft Azure e Databricks para processamento de transições bancários

## Escopo do projeto 
Este projeto visa a cronstrução de toda a arquitetura, fluxo e processamento de dados de transições bancárias de um banco fictcio utilizando das mais diversas funções disponibilizadas pela cloud Azure e Linguagem Python.

## Arquitetura do projeto 
O projeto utiliza a arquitetura em nuvem da Microsoft Azure.O Azure oferece recursos e ferramentas para ajudar no desenvolvimento e implantação de aplicativos, além de garantir alta disponibilidade, segurança e desempenho.

![image](https://github.com/thiagothr/Azure-Databricks-Analise-Bancario/assets/72639507/d5948703-4130-487d-a0e1-7f6d0591dd0b)

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

![image](https://github.com/thiagothr/Azure-Databricks-Analise-Bancario/assets/72639507/206ccd73-0985-4409-b26b-50765362dabf)

- Nesta etapa são realizados a criação de scripts utilizando PySpark para fazer a conexão do Storage Account com o Databricks e leitura do dataset CSV e implementação de regras de negócio para processar os dados de forma precisa, para então realizar a conexão com o Azure SQL database disponibilizando os dados através de tabelas estruturadas para facilitar a disponibilização para quem utiliza de soluções de analises para como Power BI.

- O próximo passo é iniciar a realização da fase de processamento dos dados armazenados. E para isto, é criado um workspace no DATABRICKS.

![image](https://github.com/thiagothr/Azure-Databricks-Analise-Bancario/assets/72639507/16423cd0-216c-48b0-8cd0-f32ba013769f)

- Na imagem acima é criado um cluster no Databricks com as configurações um pouco mais básicas pois a carga de processamento do nosso projeto não precisa de maiores configurações.

- Nesta etapa são realizados a criação de scripts utilizando PySpark como conexão do Storage Account com o Databricks e leitura do dataset CSV e implementação de regras de negócio para processar os dados de forma precisa para então realizar a conexão com o Azure SQL database disponibilizando os dados através de tabelas estruturadas para facilitar a disponibilização para quem utiliza de soluções de analises para como Power BI.

## mount entre azure storage account com o databricks
![image](https://github.com/thiagothr/Azure-Databricks-Analise-Bancario/assets/72639507/a8230cde-d15f-46d7-b0ee-c376913b9972)

- Além do script criado foi também configurado e criado o SecretScope para armazenar usuário e senhas para fim de ter um segurança dentro da ferramenta


![image](https://github.com/thiagothr/Azure-Databricks-Analise-Bancario/assets/72639507/19f6c5fb-b3ef-4aa7-b275-3de744d9e9f8)


## Filtragem dos clientes que tem o maior limite e que tiveram transições acima de 4000 reais
![image](https://github.com/thiagothr/Azure-Databricks-Analise-Bancario/assets/72639507/8ce2f4f9-80f3-4258-926e-483731d66d2c)

## Conexão do Azure databricks com Azure SQL Database
![image](https://github.com/thiagothr/Azure-Databricks-Analise-Bancario/assets/72639507/afe3ada5-e808-467f-8293-3bbafc28daa4)

- Então após a criação de todo o script e conexão com o banco do Azure na imagem abaixo pode ver todo o dataset gerado no databricks estruturado no banco para então ser disponibilizado para analises e criações de dashboard.

![image](https://github.com/thiagothr/Azure-Databricks-Analise-Bancario/assets/72639507/f4728d21-fe02-4396-8929-775bb0343ffd)


