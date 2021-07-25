:spiral_calendar: Atualizado em 25 de junho de 2021 :heart:

<img align="right" alt="GIF" height="160px" src="https://github.com/rdeconti/rdeconti-resources/blob/main/under_construction.gif" />

:blush: Este projeto está em estudo. Carga inicial realizada para manter cópia de segurança :blush:

<img align="right" alt="GIF" height="160px" src="https://github.com/rdeconti/rdeconti-resources/blob/main/Digital%20Innovation%20One%20-%20Logotipo.png" />

# Projeto Digital Innovation One - Criando um Ecossistema Hadoop Totalmente Gerenciado com Google Cloud Dataproc 
Este projeto foi proposto pela Digital Innovation One
- Link do código original: https://github.com/cassianobrexbit/DIO-LiveCoding-AWS-BigData
- Professora: Cassiano Peres
- Aula: https://web.digitalinnovation.one/project/criando-seu-ecossistema-de-big-data-na-nuvem/learning/87c89b13-07ba-4f94-a2fe-3776cfc1356c?back=/track/cognizant-cloud-data-engineer

## Descrição
Com base no repositório disponibilizado pelo expert (https://github.com/cassianobrexbit/DIO-LiveCoding-AWS-BigData), te desafiamos a replicar e, porque não, melhorar o algoritmo de extração/contabilização de palavras. Para isso, você pode ordenar as palavras por ocorrência e não por ordem alfabética (apresentando as mais citadas no texto com prioridade), por exemplo. Sinta-se à vontade para evoluir o algoritmo de outras formas ;)

## Descrição do projeto original
# DIO-LiveCoding-AWS-BigData
Repositório de cógido do Dio Live Coding com AWS EMR e Python
Neste repositório há os arquivos de configuração e execução de análise de dados.

## Instruções

* Acessar S3: https://s3.console.aws.amazon.com/s3/ 
  * Criar estrutura de data lake : _dio-live-datalake_
  * Criar estrutura de pastas:
    * _data_
    * _output_
    * _temp_
* Acessar EMR: https://console.aws.amazon.com/elasticmapreduce/
    * O cluster será criado pelo MrJob e não pelo console
    * Infraestrutura como código 
* Criar chave SSH
    * Acessar  Console do EC2: https://console.aws.amazon.com/ec2/ -> Key Pairs -> Create Key Pair	
    * Download .pem file
* Obter Id e chave secreta AWS para configurar MrJob
   * Profile
   * My Security Credentials: https://console.aws.amazon.com/iam/home?region={region}#/security_credentials
   * Access Keys - Create new access key
   * Fazer download - única chance de visualizar
* Ambiente linux
   * Criar ambiente virtual python: _virtualenv --python=python3.6 venv_diolive_
   * Acessar com o vs code
* Instalar vscode no Ubuntu
   *  code .
* Criar algoritmo de análise de palavras
   * dio-live-wordcount-test.py
   * map-reduce-count : contar
   * Instalar boto3: _pip install boto3_
   * Instalar mrjob: _pip install mrjob_
* Acessar S3
   * Upload de arquivo para o bucket
* Ambiente virtual python: source venv_teste/bin/activate
  * _nano ~/.mrjob.conf_
  * _python3 dio-live-wordcount-test.py -r emr s3://{your_s3_bucket_name}/data/SherlockHolmes.txt --output-dir=s3://{your_s3_bucket_name}/output/logs1 --cloud-tmp-dir=s3://{your_s3_bucket_name}/temp/_

