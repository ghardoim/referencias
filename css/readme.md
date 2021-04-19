[back](../readme.md)
# [CSS](https://www.w3schools.com/cssref/css_selectors.asp)
## Sintaxe de seletores em CSS
```css
  tag {}                            /* pela tag HTML */
  
  .classe {}                        /* pela classe */
  
  #id {}                            /* pelo id */
  
  *                                 /* todos os itens*/
  
  ,                                 /* vários itens */
  
  .itemA.itemB                      /* que possuam ambas classes (ou ids)  */
  
  .itemA .itemB                     /* onde B é filho de A  */
  
  itemA > itemB                     /* o B que for filho do A  */
  
  itemA + itemB                     /* o 1° B imediatamente depois do A */
  
  itemA ~ itemB                     /* o B precedido por A */
  
  itemA[atributo]                   /* que possua o atributo */
  
  [atributo=valor]                  /* que o atributo tenha esse valor */
  
  [atributo~=valor]                 /* contenha */
  
  [atributo^=valor]                 /* comece */
  
  [atributo$=valor]                 /* termine */
  
  [atributo*=valor]                 /* substring */
  
  :empty                            /* elementos sem conteúdo */
  
  :hover                            /* quando o mouse passar por cima */
  
  :not(seletor)                     /* inverte a seleção */
  
```