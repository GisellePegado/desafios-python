# Estruturas Condicionais (Conditional Statements)

## O que é

Estruturas condicionais permitem que um programa tome decisões em tempo de execução: executar um trecho de código apenas se uma determinada condição for verdadeira. Em Python, isso é feito com as palavras-chave `if`, `elif` (else if) e `else`.

O bloco `if` é avaliado primeiro. Se a condição for `True`, seu corpo é executado e os demais blocos são ignorados. O `elif` oferece condições alternativas, verificadas em ordem. O `else` é o bloco padrão, executado quando nenhuma das condições anteriores for satisfeita. A indentação em Python delimita os blocos — ao contrário de outras linguagens que usam chaves `{}`.

Condicionais são essenciais para implementar regras de negócio, validações e lógica de ramificação em qualquer programa.

## Como é usado neste projeto

Em `codigo_1.py`, o `if/elif/else` determina a porcentagem do plano de saúde de acordo com a faixa etária do cliente. Em `codigo_2.py`, condicional aninhada decide o preço da pizza com base no sabor e no tamanho. Em `codigo_3.py`, uma cadeia de condicionais mapeia o tipo de madeira ao seu preço por m³ e calcula o percentual de desconto conforme a quantidade pedida.

## Exemplo do projeto

```python
# codigo_1.py — faixa etária determina o multiplicador do plano
def calcular_porcentagem(idade):
    if idade >= 0 and idade < 19:
        return 100 / 100
    elif idade >= 19 and idade < 29:
        return 150 / 100
    elif idade >= 29 and idade < 39:
        return 225 / 100
    elif idade >= 39 and idade < 49:
        return 240 / 100
    elif idade >= 49 and idade < 59:
        return 350 / 100
    else:
        return 600 / 100
```

## Recursos para aprofundamento

- [if Statements – Python Docs](https://docs.python.org/3/tutorial/controlflow.html#if-statements) — documentação oficial sobre condicionais
- [Python Conditions – W3Schools](https://www.w3schools.com/python/python_conditions.asp) — introdução prática com exemplos interativos
