
# Sumário

Esta aplicação web foi desenvolvida pela Marta Pereira e pelo Francisco Ribeiro para a cadeira de Base de Dados (CC2005).
O intuito deste trabalho é facilitar a escolha de uma garrafa de vinho permitindo a consulta de vários atributos, bem como a sua classificação.

Os dados foram extraídos do [Blog dos vinhos] (https://osvinhos.blogspot.com/).
Dados recolhidos por Luís Oliveira (https://data.world/loliveira1999/portuguese-wine-dataset-from-blogosvinhos).

#  Referência

- [PyMySQL](https://pymysql.readthedocs.io/)
- [Flask](https://flask.palletsprojects.com/en/2.0.x/)
- [Jinja templates](https://jinja.palletsprojects.com/en/3.0.x/)


# Instalação de dependências

## Python 3 e pip 

Deve ter o Python 3 e o gestor de pacotes pip instalado. Pode
instalar os mesmos em Ubuntu por exemplo usando:

```
sudo apt-get install python3 python3-pip
```

## Bibliotecas Python

```
pip3 install --user Flask PyMySQL cryptography
```


# Configuração da BD

Edite o ficheiro `db.py` no que se refere à configuração da sua BD, modificando os parâmetros `DB` (nome da base de dados), `USER` (nome do utilizador) e `PASSWORD` (senha do utilizador).


# Execução

Inicie a aplicação executando `python3 server.py` e interaja com a mesma
abrindo uma janela no seu browser  com o endereço [__http://localhost:9001/__](http://localhost:9001/) 

```
$ python3 server.py
2021-11-27 15:07:33 - INFO - Connected to database movie_stream
 * Serving Flask app "app" (lazy loading)
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: off
2021-11-27 15:07:33 - INFO -  * Running on http://0.0.0.0:9001/ (Press CTRL+C to quit)
SELECT COUNT(*) AS movies FROM MOVIE
2021-11-27 15:07:37 - INFO - SQL: SELECT COUNT(*) AS movies FROM MOVIE Args: None
SELECT COUNT(*) AS actors FROM ACTOR
2021-11-27 15:07:37 - INFO - SQL: SELECT COUNT(*) AS actors FROM ACTOR Args: None
```



