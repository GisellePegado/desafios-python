# Funções (Functions)

## O que é

Funções são blocos de código reutilizáveis que executam uma tarefa específica. Em Python, uma função é definida com a palavra-chave `def`, seguida do nome, parâmetros entre parênteses e dois pontos. O corpo da função é indentado e pode retornar um valor com `return`.

O uso de funções é um dos princípios fundamentais da programação estruturada: em vez de repetir o mesmo código em vários lugares, encapsulamos a lógica em uma função e a chamamos sempre que necessário. Isso torna o código mais legível, mais fácil de testar e de modificar.

Funções também permitem dividir problemas complexos em partes menores e bem definidas — cada função tem uma responsabilidade clara, o que facilita a leitura e manutenção do programa.

## Como é usado neste projeto

Todos os quatro arquivos do projeto organizam sua lógica em funções. Em `codigo_1.py`, as funções `calcular_porcentagem()` e `calcular_valor_mensal()` isolam os cálculos do plano de saúde. Em `codigo_2.py`, `calcular_valor()` e `imprimir_pedido()` tratam a lógica da pizzaria. Em `codigo_3.py`, diversas funções auxiliares organizam cada etapa da compra de madeira. Em `codigo_4.py`, funções genéricas como `imprimir_menu()` e `consultar_por_parametro()` são reutilizadas em contextos diferentes.

## Exemplo do projeto

```python
# codigo_1.py
def calcular_porcentagem(idade):
    if idade >= 0 and idade < 19:
        return 100 / 100
    elif idade >= 19 and idade < 29:
        return 150 / 100
    # ...

def calcular_valor_mensal(valorBase, porcetagem):
    return valorBase * porcetagem

# Chamada das funções no programa principal
porcentagem = calcular_porcentagem(idade)
valorMensal = calcular_valor_mensal(valorBase, porcentagem)
```

## Recursos para aprofundamento

- [Defining Functions – Python Docs](https://docs.python.org/3/tutorial/controlflow.html#defining-functions) — documentação oficial sobre funções em Python
- [Python Functions – Real Python](https://realpython.com/defining-your-own-python-function/) — guia completo com exemplos práticos
