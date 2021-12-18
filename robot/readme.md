[back](../readme.md)
# [Robot](https://robotframework.org/)
## Sintaxe do Robot
* **<ins>pip install robotframework</ins>**: Instalação do Robot Framework
---
```python
    *** Settings ***                        #import de libraries e referência de resources
    *** Variables ***                       #definição de variáveis globais
    *** Keywords ***                        #implementação das keywords próprias
    *** Test Cases ***                      #implementação do processo
    [Arguments]                             #parâmetros utilizados pelas keywords
    [Return]                                #valor de retorno de uma keyword
    ...                                     #continuação de um comando
```
### Tipo de Variáveis
```python
    ${VAR_NAME}         valor                       #variável simples
    @{VAR_LIST}         valor1      valor2          #variável lista
    &{VAR_DICT}         chave=valor                 #variável dicionário
```