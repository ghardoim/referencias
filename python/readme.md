[back](../readme.md)
# [Python](https://www.python.org/doc/)
## Sintaxe do Python
* **snake_case**: Padrão de nomenclatura.
* **<ins>python -m venv</ins> dir_name**: Cria um ambiente virtual para manter as dependências locais no projeto.
* **<ins>source</ins> dir_name<ins>/Script/activate</ins>**: Ativa o ambiente virtual criado.
* **<ins>deactivate</ins>**: Desativa o ambiente virtual. 
* **<ins>pip install</ins> pacote**: Instala um pacote de dependência.
* **<ins>python -m pip install --upgrade pip</ins>**: Atualiza o pip.
* **<ins>pyinstaller -w</ins> arquivo.py**: Gera o executável de um script simples.
* **<ins>auto-py-to-exe</ins>**: Gera o executável de um script mais robusto.
* **<ins>r"</ins>string<ins>"</ins>**: Raw string. Usar quando informar paths.
* **<ins>f"{</ins>string<ins>}"</ins>**: Format string.
---
```python
  from lib import pacote as apelido
```
### Operadores lógicos
```python
  True / False
  not   #não
  and   #e
  or    #ou
  in    #em
  ==    #igual
  !=    #diferente
  >     #maior que
  >=    #maior ou igual
  <     #menor que
  <=    #menor ou igual
  **    #potenciação
```
### Declaração de variáveis
```python
  del variavel        #remove o objeto
  variavel = None     #objeto nulo
  variavel = []       #lista
  variavel = ()       #tupla
  variavel = {}       #dicionário
  / int / float / str / bool / list / tuple / dict / object 

  with open("path_arquivo", "r | w | a") as arquivo:
```
### Condicionais
```python
  if condição:
    ...
  elif condição:
    ...
  else:
```
### Repetições
```python
  for i, item in enumerate(lista):    #unpack
    ...
    break
```
```python
  while condição:
    ...
    continue
```
#### List Comprehension
```python
  lista = [ expressão for item in iterable if codição ]                               #cria uma nova lista filtrada
```
```python
  lista = [ expressão if condição else outra_expressão for item in iterable ]         # //  //   //   //   de mesmo tamanho
```
### Funções
```python
  def nome(parametro: tipo) -> tipo_retorno:               #annotations
    pass
```
```python
  def nome(parametro, *args):                              #uma tupla de positional arguments
    ...
```
```python
  def nome(parametro, **kwargs):                           #um dicionário de keywords arguments
    ...
```
#### Lambda Expressions
```python
  nova_função = lambda parametro: expressão_retorno        #nova_função(parametro)
```
```python
  def função_lambda(parametro):
    return lambda argumento: argumento + parametro
  nova_função = função_lambda(parametro)                   #nova_função(argumento)
```
### Tratamento de erros
```python
  try:
    ...
  except TipoDoErro as erro:
    raise Exception()                 #lança uma exception
    ...
  else:                               #caso não dê erro
    ...
  finally:                            #com ou sem erro
    ...
```
### Integrações
#### Pandas
```python
  import pandas as pd
  import pandas_datareader.data as pd_dr
  import matplotlib.pyplot as plt
  import numpy as np

  dataframe = pd.read_ [csv, json, excel] (nome_arquivo, sep = ";")
  novo_df = dataframe["nome_coluna"][linha]
  
  filtra_df = dataframe.loc[linha, coluna]            # ':' -> todas | 'where' -> de acordo com condição

  pd.to_ [csv, json, excel] (nome_arquivo, sep = ";")
```
#### Path
```python
  from pathlib import Path
  caminho = Path.cwd() / Path("arquivo")                 # concatena Paths
```
#### Email
##### Gmail
```python
  import yagmail
  usuario = yagmail.SMTP(email, senha)
  usuario.send(to = [], subject = "", contents = "", attachment = [])
```
##### Outlook
```python
  import win32com.client as win32                        # integração com o pacote office
  
  outlook = win32.Dispatch("outlook.application")
  email = outlook.CreateItem(0)                          # mesmo processo do VBA
```
#### SQL
```python
  import pyodbc
  dados_conexao = ("Drive={};Server=NomeServidor;Database=NomeBaseDeDados")
  conexao = pyodbc.connect(dados_conexao)
  
  import pandas as pd  
  sql_df = pd.read_sql("CONSULTA SQl", conexao)
```
#### SQL
```python
  from selenium.webdriver.common.keys import Keys                         # Keys.RETURN - Enter
  from selenium import webdriver
  drive = webdriver.Navegador()                                           # .Chrome() / .Edge() / .Firefox()

  elemento = drive.find_element_by_ [id, classe, tag, name, xpath]        # retorna 1 elemento
  elementos = drive.find_elements_by_ [classe, tag, name, xpath]          # retorna uma lista
```
#### APIs
```python
  import requests
  import json

  resposta = requests.get("")                         # retorna o HTTP Status Code
  resposta_dict = resposta.json()                     # transforma a resposta json em dicionário python
```
#### Twilio
```python
  from twilio.rest import Client
  client = Cliente(account_sid, token)
  mensagem = client.messages.create(to = destino, from_ = remetente, body = "")         # destino é um número verificado.
```
#### ArcGis
- `conda install -c esri arcgis`
```python
  from arcgis.gis import GIS
  from arcgis.mapping import WebMap
```