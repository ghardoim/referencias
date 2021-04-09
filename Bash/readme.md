[back](../readme.md)
# Comandos Bash
## Linha de comandos para teminais baseados em Linux.

* **<ins>echo -n</ins>**: Imprime na tela sem pular linha.
* **_comando_ <ins>\></ins> _arquivo_**: Substitui o conteúdo do arquivo com a saída do comando.
  * **_comando_ <ins>&\></ins> _arquivo_**: Saída de erros.
* **_comando_ <ins>\>\></ins> _arquivo_**: Apenda no conteúdo do arquivo a saída do comando.
  * **_comando_ <ins>&\>\></ins> _arquivo_**: Saída de erros.
* **_comando1_ <ins>|</ins> _comando2_**: Passa a saída de um comando para o outro.
* **<ins>\<$(</ins>_comando_<ins>)</ins>**: SubShell. Redireciona a saída para o comando pai.
* **<ins>whoami</ins>**: Retorna o nome do usuário logado.
* **<ins>curl</ins>**: Usado para realizar requisições HTTP.
* **<ins>touch</ins> _nomearquivo_**: Usado para criar arquivos.
* **<ins>mkdir</ins> _nomediretório_**: Usado para criar diretórios.
* **<ins>diff -y</ins> _arquivo1_ _arquivo2_**: Mostra a diferença entre dois arquivos.
* **<ins>grep</ins> _pattern_**: Filtra a entrada dada de acordo com a expressão regular passada.
  * **<ins>-v</ins>**: Filtra o que não bater com a expressão regular.
  * **<ins>-w</ins>**: Filtra apenas se a expressão regular bater com uma palavra inteira.
  * **<ins>-i</ins>**: Não diferencia entre maiúsculas e minúsculas.
* **<ins>ls -Slha --time-style=+"%Y-%m-%d %H:%M"</ins>**: Lista o conteúdo do diretório corrente em ordem decrescente de tamanho numa saída de alto nível.
* **<ins>pwd</ins>**: Retorna o path completo do diretório atual.
  * **<ins>-W</ins>**: Retorna o path no formato Windows.
* **<ins>sleep</ins> _tempo_**: Pausa o terminal por determinado tempo.
* **<ins>date +"%</ins>_formato_<ins>" --date=</ins>_referencia_**: Retorna a data da referência no formato indicado.
* **<ins>stat -c "%.10w %.10y"</ins> _arquivo_**: Exibe a data de criação e da última modificação.
* **<ins>awk -F"</ins>_pattern_<ins>" '{ print $</ins>_item_<ins>}'</ins>**: Divide a entrada numa lista de acordo com a expressão passada e exibe a saída de acordo com o item pedido.
* **<ins>wc -lmw</ins>**: Mostra a quantidade de linhas, palavras e caracteres.
* **<ins>head -n</ins>**: Mostrad as primeiras _n_ linhas.
* **<ins>sort -du</ins> _arquivo_ <ins>-o</ins> _arquivo_**: Organiza o arquivo em ordem alfabética sem linhas repetidas e sobreescreve.
* **<ins>cp</ins> _origem_ _destino_**: Copia arquivos.
* **<ins>mv</ins> _origem_ _destino_**: Move arquivos.
* **<ins>rm -r</ins> _arquivo_**: Deleta arquivos.
* **<ins>read</ins> _variavel_**: Armazena entrada de dados do teclado.
* **<ins>expr</ins> _expressao_**: Realiza expressões aritméticas, lógicas e em strings.
* **<ins>let</ins> _expressao_**: Realiza expressões incrementais.
* **<ins>find . -iname</ins> _pattern_ <ins> | xargs</ins> _cmd_**: Procura a partir do diretório atual por arquivos com o pattern no nome, não diferenciando maiúsculas de minúsculas, e passa cada um deles como entrada para o comando seguinte.
* **<ins>basename</ins> _path_**: Retorna o último componente do diretório.
* **<ins>dirname</ins> _path_**: Retorna o path completo do diretório pai.
* **<ins>tr -d</ins> _pattern_**: Remove do argumento passado aquilo que bater com o pattern.
* **<ins>which</ins> _comando_**: Retorna a localização do comando.
* **<ins>history</ins> _comando_**: Lista os comandos executados.
* **<ins>!!</ins>**: Executa o último comando do histórico.
* **<ins>clear</ins> _comando_**: Limpa o terminal.
* **<ins>chmod -R +x 777</ins>**: Torna executável e dá todas as permissões recursivamente.
* **<ins>du -hs</ins>**: Retorna o tamanho em alto nível do diretório atual não recursivamente.
* **<ins>exit</ins> _status_**: Encerra o terminal atual com o status informado.
* **<ins>eval</ins> _texto_**: Executa o texto como um comando.
* **<ins>tar -cf</ins> _arquivo_<ins>.tar</ins> _diretorio_**: Comprime os arquivos do diretório especificado.