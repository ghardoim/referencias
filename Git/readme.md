[back](../readme.md)
# [Git CLI](https://git-scm.com/)
## Gerenciador de código fonte
- **<ins>git</ins>**
  * **<ins>status</ins>**: Mostra quais arquivos foram modificados.
  * **<ins>add</ins>**
    * **<ins>.</ins>**: Adiciona todos os arquivos no próximo pacote a ser commitado.
    * **_nomearquivo_**: Adiciona um arquivo específico. 
  * **<ins>commit</ins>**
    * **<ins>-am</ins> _mensagem_**: Realiza o commit com todos os arquivos.
    * **<ins>--amend</ins>**: Edita a mensagem do último commit.
  * **<ins>diff</ins>**
    * **_hashrecente_<ins>..</ins>_hashantigo_**: Mostra a diferença entre dois commits.
    * **<ins>--raw</ins> _nometag_**: Mostra o estado dos arquivos naquela tag.
  * **<ins>rebase -i</ins> _hashorbranch_**: Organiza o histórico de commits.
  * **<ins>tag</ins>**
    * **<ins>--sort=-creatordate --format="%(creatordate:short)%09%(refname:strip=2)</ins>**: Lista as tags da recente à antiga exibindo a data e o nome.
    * **<ins>-n</ins>**: Lista a nome da tag e sua mensagem.
    * **<ins>-a</ins> _nometag_ <ins>-m</ins> _mensagem_**: Cria uma nova tag com a mensagem.
  * **<ins>log</ins>**
    * **<ins>":(exclude)*.</ins>_pattern_<ins>"</ins>**: Ignora extensões de arquivos.
    * **<ins>--all</ins>**
      * **<ins>--diff-filter=A --</ins> _nomearquivo_**: Mostra o commit que adicionou o arquivo.
      * **<ins>--follow</ins> _nomearquivo_**: Lista todos os commits que tenham o arquivo.
    * **<ins>--no-merges</ins> _tag_<ins>...</ins>_tag_ <ins>--date=format:"%Y-%m-%d" --pretty=format:"%B;%aN;%ad"</ins>**: Lista os commits, autores e datas entre duas tags sem merges.
  * **<ins>rev-list</ins> _hashcommit_**: Lista os hashs dos commits.
  * **<ins>shortlog -s --email</ins>**: Lista os autores, seus emails e quantos commits fizeram.
  * **<ins>remote get-url</ins> _origin_**: Mostra a URL do repositório remoto.
  * **<ins>checkout -b</ins>** | **<ins>switch -c</ins>**: Cria e muda para uma nova branch.
  * **<ins>branch</ins>**
    * **<ins>-a --contains</ins> _hash_**: Lista as branchs que contém o commit.
    * **<ins>-D</ins> _nomebranch_**: Deleta uma branch localmente.
  * **<ins>push</ins>**
    * **<ins>-u</ins> _branchremota_ _branchlocal_**: Sincroniza repositório local com o remoto.
    * **_repositorioremoto_**
      * **_branchlocal_<ins>:</ins>_branchremota_**: Aponta branch local para uma branch remota.
      * **<ins>--delete</ins> _nomebranch_**: Deleta uma branch remota.
    * **<ins>--tags</ins>**: Envia as tags para o repositório remoto.
  * **<ins>archive</ins> _nometag_ <ins>--format=zip --output=</ins>_nomearquivo_<ins>.zip</ins>**: Gera um pacote zip do repositório no estado da tag.
  * **<ins>blame</ins> _arquivo_**: Mostra quem e quando modificou o arquivo.
  * **<ins>restore --source=</ins>_hashcommit_ _nomearquivo_**: Muda o arquivo especificado para o estado em que ele estava naquele commit.
  * **<ins>revert</ins> _hashcommit_**: Desfaz as alterações daquele commit.
  * **<ins>cherry-pick</ins> _hashcommit_**: Traz um commit para a branch atual.
  * **<ins>config</ins>**
    * **<ins>--global</ins>**: Define as configurações para todos os repositórios.
    * **<ins>--local</ins>**: Define configurações apenas para o repositório onde está sendo executado.

- Arquivos auxiliares:
  * **<ins>.gitignore</ins>**: O Git **não** monitora os arquivos listados aqui.
  * **<ins>.gitkeep</ins>**: Para monitorar diretórios vazios.
  * **<ins>.gitconfig</ins>**: Para configurações como user, email e alias.