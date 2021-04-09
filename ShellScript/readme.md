[back](../readme.md)
# [Shell Script](https://pt.wikipedia.org/wiki/Shell_script)
## Sintaxe de arquivos .sh

* **<ins>#!/bin/bash</ins>**: Interpretador dos comandos. Primeira linha de qualquer arquivo .sh
* **<ins>$#</ins>**: Armazena a quantidade de argumentos passados.
* **<ins>$$</ins>**: Armazena o ID do script que está em execução.
* **<ins>$@</ins>**: Armazena os valores de todos os argumentos passados.
* **<ins>$0</ins>**: Nome do script que está sendo executado.
* **<ins>$?</ins>**: Guarda o status de saída do comando antecedente.
* **<ins>$(</ins>_comando_<ins>)</ins>**: SubShell. Para guardar a saída de um comando numa variável.
---
* **<ins>#</ins>**: Indica que a linha é um comentário.
* **_comando1_ <ins>;</ins> _comando2_**: Para escrever dois comandos na mesma linha.
* **<ins>source</ins> _arquivo_<ins>.sh</ins>**: Executa um arquivo no processo atual, permitindo o acesso a variáveis e funções do mesmo.
---
### Operadores lógicos
```bash
  !   #não
  -a  #e
  -o  #ou
  -eq #igual
  -ne #diferente
  -gt #maior que
  -ge #maior ou igual
  -lt #menor que
  -le #menor ou igual
  -z  #string vazia
  -d  #é diretório
  -f  #é arquivo
  -r  #consegue ler o arquivo
  -w  #consegue escrever no arquivo
  -x  #consegue executar o arquivo
```
### Condicionais
```bash
  if [[ condição ]] then
    ...
  elif [[ condição ]] then
    ...
  else
    ...
  fi
```
```bash
  case codição in
    pattern)
      ...
    ;;
    *) #default
      ...
    ;;
  esac
```
### Repetições
```bash
  while condição #enquando
  do
    break
    ...
  done
```
```bash
  for variavel in lista #para cada
  do
    continue
    ...
  done
```
```bash
  select variavel in lista #para cada, escolha um
  do
    shift #próxima variável
    ...
  done
```
### Funções
```bash
  nome_função () { 
    ...
    return
  }
```