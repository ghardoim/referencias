[back](../readme.md)
# [Docker CLI](https://www.docker.com/)
## Gerenciador de containers (ambiente como código)
- **<ins>docker</ins>**
  * **<ins>run</ins> _flags_ _imagem_ _comando_**
    * **<ins>-it</ins> _nomecontainer_**: Sobe um container e conecta com o terminal corrente. 
    * **<ins>-w</ins> _pathcontainer_**: Path onde o container vai ser startado. 
    * **<ins>--name</ins> _nome_**: Nomea o container.
    * **<ins>--env</ins> _nomevariavel_<ins>=</ins>_valor_**: Define variáveis de ambiente dentro do container.
    * **<ins>--network</ins> _nomerede_**: Conecta o container na rede informada.
    * **<ins>-p</ins> _portalocal_<ins>:</ins>_portacontainer_**: Mapea uma porta do host local com uma do container.
      * **<ins>-P</ins>**: Realiza o mapeamento de porta de forma automática e aleatória.
    * **<ins>-d</ins> _nomecontainer_**: Sobe um container sem travar o terminal. 
    * **<ins>-v</ins> _pathlocal_<ins>:</ins>_pathcontainer_**: Realiza dos diretórios para volumes.
      * **<ins>$(pwd -W)</ins>**: Usar no _pathlocal_ quando no Windows.
  * **<ins>ps</ins>**: Lista os containers ativos.
    * **<ins>-a</ins>**: Lista todos os containers.
  * **<ins>container prune</ins>**: Remove todos os container parados.
  * **<ins>kill</ins> _idcontainer_**: Remove um container que está ativo.
  * **<ins>stop</ins> _idcontainer_**: Para um container que está ativo.
    * **<ins>-t 0 $(docker ps -q)</ins> _idcontainer_**: Para, em 0 segundos, os containers ativos.
  * **<ins>start -a -i</ins> _idcontainer_**: Ativa um container parado e vincula o terminal nele.
  * **<ins>rmi</ins>**: Remove imagens armazenadas localmente.
  * **<ins>build -f</ins> _dockerfile_ <ins>-t</ins> _dockerhub_ _pathdockerfile_**: Constrói uma imagem a partir do dockerfile informado.
  * **<ins>attach</ins> _idcontainer_**: Vincula o terminal local em um container ativo.
  * **<ins>exec</ins> _idcontainer_ _comando_**: Executa um comando no container indicado.
  * **<ins>network create --driver bridge</ins> _nomerede_**: Cria uma rede para comunicação entre containers.
  * **<ins>cp</ins> _pathlocal_<ins>/</ins>_arquivo_ _idcontainer_<ins>:</ins>pathcontainer**: Copia arquivos para dentro do container.
  * **<ins>rename</ins> _idcontainer_ _novonome_**: Renomeia o container.