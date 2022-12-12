# DataPipeline Twitter 🐦
## _Pipeline de Dados utilizando Airflow_

- Utiliza a API gratuita do Twitter para coleta de tweets
- Criação de um Airflow Hook e Airflow Operator
- Orquestração via Airflow

### instalação PIP:
```
sudo apt install python3-pip
```
### instalação venv
```
pip install virtualenv
```
### iniciando virtual environment pela primeira vez

```
python3.9 -m venv venv
```

### entrando no virtual environment

```
source venv/bin/activate
```
### instalando airflow

```
AIRFLOW_VERSION=2.3.2
```
```
PYTHON_VERSION=3.9
```
```
CONSTRAINT_URL="https://raw.githubusercontent.com/apache/airflow/constraints-${AIRFLOW_VERSION}/constraints-${PYTHON_VERSION}.txt"
```
```
pip install "apache-airflow[postgres,celery,redis]==${AIRFLOW_VERSION}" --constraint "${CONSTRAINT_URL}"
```

### executar airflow

```
airflow standalone
```
### exportar váriavel de ambiente do airflow home
```
export AIRFLOW_HOME=~/DataPipelineTwitter/airflow
```

### criar uma conexão via airflow

###### Dentro da GUI do Aiflow, utilize a área connections para criar uma conexão nova.
###### em "connection_id", coloque "twitter_default"
###### em Connection Type, escolha "HTTP";
###### em Host, coloque "https://api.twitter.com";
###### no campo Extra, coloque "{"Authorization":"Bearer XXXX"}", trocando XXXX pelo Bearer Token.
###
### saindo da venv
```
deactivate
```
