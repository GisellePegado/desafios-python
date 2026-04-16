# Laços de Repetição (Loops)

## O que é

Laços de repetição permitem executar um bloco de código várias vezes. Python oferece dois tipos principais: `while` e `for`. O `while` repete enquanto uma condição for verdadeira — útil quando o número de iterações não é conhecido de antemão. O `for` itera sobre uma sequência (lista, range, string, etc.) — útil quando se sabe exatamente quais elementos percorrer.

O `while True` com `break` é um padrão comum para criar laços que continuam até que uma condição interna seja satisfeita, como a entrada de um dado válido pelo usuário. Já o `for` com `range()` gera sequências numéricas, e o `for` sobre coleções percorre cada elemento diretamente.

## Como é usado neste projeto

Em `codigo_2.py`, um `while algoMais == True` repete o ciclo de pedidos até que o cliente indique que não quer mais nada. Em `codigo_3.py`, um `while True` com `break` controla a leitura da quantidade de toras. Em `codigo_4.py`, um `for contato in lista_contatos` percorre todos os contatos para listagem e busca. O `for i in range(n_alternativas)` em `imprimir_menu()` numera dinamicamente as opções do menu.

## Exemplo do projeto

```python
# codigo_2.py — while controla múltiplos pedidos
acumulador = 0
algoMais = True

while algoMais == True:
    sabor = input('Entre com o sabor desejado (PS/PD): ')
    # ...
    acumulador += valor
    desejaAlgoMais = input('Deseja mais alguma coisa? (S/N): ')
    if desejaAlgoMais == 'N':
        algoMais = False
        print(f'O valor total a se pago: R$ {acumulador:.2f}')

# codigo_4.py — for percorre a lista de contatos
for contato in lista_contatos:
    print(f'Id: {contato["Id"]}')
    print(f'Nome: {contato["Nome"]}')
```

## Recursos para aprofundamento

- [for and while Loops – Python Docs](https://docs.python.org/3/tutorial/controlflow.html#for-statements) — documentação oficial sobre laços em Python
- [Python Loops – Real Python](https://realpython.com/python-for-loop/) — guia detalhado com exemplos de for e while
