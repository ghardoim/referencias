[back](../readme.md)

[Projeto de Estruturas de Dados](https://github.com/ghards/estruturas-de-dados-em-c)

### Declaração de variáveis
```c
  typedef struct livro { 
    char titulo[30];
    char autor[10]; 
    float preco;
    int id;
  } LIVRO;

  LIVRO *book;
```
### Condicionais
```c
  if ( condição ) {
    ...
  } else if ( condição ) {
    ...
  else {
    ...
  }
```
```c
  switch ( expressão ) {
    case valor :
      ...
      break;

    default :
      ...
  }
```
### Repetições
```c
  for (contador; limite; incremento) {
    ...
    break;
  }
```
```c
  while ( condição ) {
    ...
  }
```
```c
  do {
    ...
    continue;
  } while ( condição )
```

### Funções
```c
void main() {}                                // função principal
```
```c
defineLivro(&livro_qualquer)                  // passa um endereço de memória de um livro

LIVRO defineLivro(LIVRO *um_livro) {          // recebe um ponteiro para um livro
  (*um_livro).titulo = "titulo";              // (*um_livro).atributo = um_livro->atributo
  um_livro->autor = "autor";
  (*um_livro).preco = 100;

  return *um_livro;
}
```