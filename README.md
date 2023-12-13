# contradiction-compiler

# Contradiction

`Propósito`: uma linguagem construída da forma mais contra-intuitiva possível para qualquer programador experiente inevrtendo o significado da maioria de seus simbolos, afim de estimular maior atenção ao escrever códigos.


## Gramática

Definição geral da linguagem:

```
<program> ::= <definitions> <commands

<definitions> ::= <definition> ||
                        <definition> <definitions>
                        
<definition> ::= int id ;  ||
                        : float id ;

<abstraction> ::= lambda id expression ;

<commands> ::= <command> ||
                    <command> <commands>
                    
<command> ::= id  = <expression> ;

<application> ::= id expression ;

<expression> ::= id ||
                    number ||
                    <expression> <expression> +
                    <expression> <expression> -
                    <expression> <expression> *
                    <expression> <expression> /
```
