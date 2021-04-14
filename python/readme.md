[back](../readme.md)
# [Python](https://www.python.org/doc/)
## Sintaxe do Python
* **snake_case**: Padrão de nomenclatura.
* **<ins>python -m venv</ins> dir_name**: Cria um ambiente virtual para manter as dependências locais no projeto.
* **<ins>source</ins> dir_name<ins>/Script/activate</ins>**: Ativa o ambiente virtual criado.
* **<ins>deactivate</ins>**: Desativa o ambiente virtual. 
* **<ins>pip install</ins> pacote**: Instala um pacote de dependência.
---
```python
  from lib import pacote as apelido
```
## Operadores lógicos
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
```
### Declaração de variáveis
```python
  variavel = None     #objeto nulo
```
### Funções
```python
  def nome(parametro: tipo) -> tipo_retorno:
    pass
```