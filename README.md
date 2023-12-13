# Contradiction Compiler

## Bem-vindo ao Mundo do Contradiction!

**Contradiction** é uma linguagem de programação inovadora e deliberadamente contra-intuitiva. Projetada para desafiar programadores experientes, esta linguagem inverte o significado da maioria dos símbolos e construções comuns, exigindo uma atenção redobrada e uma abordagem totalmente nova para escrever código. Mergulhe em um mundo onde tudo que você sabia sobre programação é virado de cabeça para baixo!

### Propósito
Nossa missão é estimular a atenção aos detalhes e oferecer um exercício mental único, invertendo o que é tradicionalmente esperado em linguagem de programação.


### Paradigma Funcional Utilizado
Crição de funções e chamadas de funções.

### Operações Aritméticas Invertidas
- `+` agora representa **subtração**
- `-` agora representa **adição**
- `*` agora representa **divisão**
- `/` agora representa **multiplicação**

### Tipos Reimaginados
- `int` representa um **ponto flutuante**
- `float` representa um **inteiro**

### Funções e Sintaxe
- `def` agora equivale a **return**
- `:` agora equivale a **sizeof**

### Símbolos Alternativos
- `;` é usado como **?**

Prepare-se para repensar a maneira como você programa e aceite o desafio de Contradiction!

## Gramática de Backus-Naur Form (BNF) da Linguagem
`devido ao caráter confuso da limguagem, alguns simbolos foram trocados pelos seus nomes de Token, a gramática no ipynb registra quais simbolos são realmente usados, omitindo a aqueles sem alterações`

Definição geral da linguagem:

```
<prog> ::= <vardecls> <statements>

<vardecls> ::= <vardecl> | <vardecl> <vardecls>

<vardecl> ::= 'INT' id 'SEP' | 'INT' id = <expression> 'SEP' | 'DEF' id 'OPEN_PARENS' id 'CLOSE_PARENS' 'INDENTATION' <expression> 'SEP'



<statements> ::= <openstatement> | <openstatement> <statements>

<openstatement> ::= id = <expression> 'SEP' 
               | 'IF' 'OPEN_PARENS' <expression> 'COMP' <expression> 'CLOSE_PARENS' <openstatement>
               | 'IF' 'OPEN_PARENS' <expression> 'COMP' <expression> 'CLOSE_PARENS' <closedstatement> 'ELSE' <openstatement>
               | 'WHILE' 'OPEN_PARENS' <expression> 'COMP' <expression> 'CLOSE_PARENS' <openstatement>
               | 'FOR' 'OPEN_PARENS' id = <expression> 'SEP' <expression> 'COMP' <expression> 'SEP' id = <expression> 'CLOSE_PARENS' <openstatement>

<closedstatement> ::= id = <expression> 'SEP'
                   | 'IF' 'OPEN_PARENS' <expression> 'COMP' <expression> 'CLOSE_PARENS' <closedstatement> 'ELSE' <closedstatement>
                   | 'WHILE' 'OPEN_PARENS' <expression> 'COMP' <expression> 'CLOSE_PARENS' <closedstatement>
                   | 'FOR' 'OPEN_PARENS' id = <expression> 'SEP' <expression> 'COMP' <expression> 'SEP' id = <expression> 'CLOSE_PARENS' <closedstatement>

<expression> ::= id
               | 'NUMBER'
               | id 'OPEN_PARENS' <expression> 'CLOSE_PARENS'
               | 'OPEN_PARENS' <expression> 'CLOSE_PARENS'
               | <expression> 'PLUS' <expression>
               | <expression> 'MINUS' <expression>
               | <expression> 'MUL' <expression>
               | <expression> 'DIV' <expression>

```
