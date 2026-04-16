# Tratamento de Exceções (Exception Handling)

## O que é

Exceções são erros que ocorrem durante a execução de um programa — por exemplo, tentar converter a string `"abc"` em inteiro com `int()` lança uma `ValueError`. Em vez de deixar o programa travar, Python permite **capturar** essas exceções com o bloco `try/except`.

O código "arriscado" fica dentro do `try`. Se uma exceção do tipo esperado ocorrer, o bloco `except` é executado em vez de interromper o programa. É possível capturar tipos específicos de exceção (como `ValueError` ou `TypeError`) para tratar cada situação de forma apropriada. Também é possível usar `raise` para lançar exceções manualmente quando uma regra de negócio é violada.

## Como é usado neste projeto

Em `codigo_3.py`, a função `qtd_toras()` usa `try/except ValueError` para capturar entradas não numéricas e entradas que excedam o limite de 2000 toras. Em `codigo_4.py`, `imprimir_menu()` usa a mesma estrutura para capturar opções de menu inválidas, e `consultar_por_id()` lança `ValueError` manualmente quando um ID digitado não existe na lista de contatos.

## Exemplo do projeto

```python
# codigo_4.py — raise manual para simular exceção de validação
def consultar_por_id():
    while True:
        try:
            id = int(input('Digite o Id do contato: '))
            if id in [contato['Id'] for contato in lista_contatos]:
                break
            else:
                raise ValueError  # lança exceção se o id não existir
        except ValueError:
            print('Id inválido')
    consultar_por_parametro('Id', id)
```

## Recursos para aprofundamento

- [Errors and Exceptions – Python Docs](https://docs.python.org/3/tutorial/errors.html) — documentação oficial sobre exceções em Python
- [Python Exceptions – Real Python](https://realpython.com/python-exceptions/) — guia prático sobre try/except, raise e exceções customizadas
