# Validação de Entrada com Loop (Input Validation Loop)

## O que é

Validação de entrada é a prática de verificar se os dados fornecidos pelo usuário atendem aos critérios esperados antes de usá-los no programa. Sem validação, entradas inválidas podem causar erros, resultados incorretos ou comportamento inesperado.

Um padrão muito comum em Python é usar um laço `while` que repete a solicitação de entrada até que o usuário forneça um valor aceitável. Combinado com `try/except`, esse padrão captura erros de conversão de tipo (como tentar converter texto em número) e exibe mensagens de orientação ao usuário, tornando o programa robusto e amigável.

## Como é usado neste projeto

O padrão de validação aparece em todos os quatro arquivos. Em `codigo_2.py`, laços `while` verificam se o sabor (`PS`/`PD`) e o tamanho (`P`/`M`/`G`) informados são válidos antes de prosseguir. Em `codigo_3.py`, o laço em `qtd_toras()` combina `while True` e `try/except ValueError` para garantir que a quantidade de toras seja um inteiro válido dentro do limite aceito. Em `codigo_4.py`, `imprimir_menu()` valida a opção escolhida e `consultar_por_id()` valida se o ID informado existe na lista.

## Exemplo do projeto

```python
# codigo_3.py — validação robusta com try/except e limite de negócio
def qtd_toras():
    while True:
        try:
            qtdToras = int(input('Entre com a quantidade de toras (m³): '))
            if qtdToras <= 2000:
                break
            else:
                print('Não aceitamos pedidos com essa quantidade de toras.')
        except ValueError:
            print('Resposta inválida.\nPor favor, entre com a quantidade novamente.\n')
    # continua com qtdToras válido...

# codigo_2.py — validação simples por comparação
sabor = input('Entre com o sabor desejado (PS/PD): ')
while sabor != 'PS' and sabor != 'PD':
    print('Sabor inválido. Tente novamente\n')
    sabor = input('Entre com o sabor desejado (PS/PD): ')
```

## Recursos para aprofundamento

- [input() – Python Docs](https://docs.python.org/3/library/functions.html#input) — documentação da função built-in `input`
- [Asking the User for Input – Real Python](https://realpython.com/python-input-output/) — boas práticas de leitura e validação de entrada do usuário
