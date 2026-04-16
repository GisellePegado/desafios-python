# Retorno Múltiplo de Funções (Multiple Return Values)

## O que é

Em Python, uma função pode retornar mais de um valor com um único `return`, separando os valores por vírgula. Internamente, Python empacota esses valores em uma **tupla** e o chamador pode desempacotá-los diretamente em variáveis distintas — uma técnica chamada **tuple unpacking** (desempacotamento de tupla).

Essa funcionalidade torna o código mais expressivo e evita a necessidade de criar estruturas auxiliares (como dicionários ou classes) apenas para retornar múltiplos resultados relacionados. É muito usada quando dois ou mais valores são calculados juntos e fazem sentido serem retornados como um par ou grupo.

## Como é usado neste projeto

Em `codigo_3.py`, a função `qtd_toras()` calcula tanto a quantidade de toras quanto o percentual de desconto correspondente. Como os dois valores dependem da mesma entrada do usuário e estão intimamente relacionados, a função os retorna juntos. O programa principal os desempacota em duas variáveis distintas com `qtdToras, desconto = qtd_toras()`.

## Exemplo do projeto

```python
# codigo_3.py — função retorna dois valores relacionados
def qtd_toras():
    # ... leitura e validação de qtdToras ...
    if qtdToras < 100:
        desconto = 0
    elif qtdToras >= 100 and qtdToras < 500:
        desconto = 4/100
    elif qtdToras >= 500 and qtdToras < 1000:
        desconto = 9/100
    else:
        desconto = 16/100
    return qtdToras, desconto  # retorno múltiplo como tupla

# Desempacotamento direto no programa principal
qtdToras, desconto = qtd_toras()
total = ((tipoMadeira * qtdToras) * (1 - desconto)) + valorTransporte
```

## Recursos para aprofundamento

- [Tuples – Python Docs](https://docs.python.org/3/tutorial/datastructures.html#tuples-and-sequences) — documentação oficial sobre tuplas e desempacotamento
- [Returning Multiple Values – Real Python](https://realpython.com/python-return-statement/#returning-multiple-values) — explicação aprofundada com exemplos de retorno múltiplo
