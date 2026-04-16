# Formatação de Strings com f-strings (f-strings / Formatted String Literals)

## O que é

F-strings (formatted string literals) são uma forma moderna e legível de incorporar expressões Python diretamente dentro de strings. Introduzidas no Python 3.6, são prefixadas com a letra `f` antes das aspas, e qualquer expressão entre chaves `{}` é avaliada em tempo de execução e inserida na string resultante.

Além de variáveis simples, as chaves podem conter expressões, chamadas de funções e **especificadores de formato**. O especificador `:.2f`, por exemplo, formata um número de ponto flutuante com exatamente duas casas decimais — essencial para exibir valores monetários de forma profissional. F-strings são mais legíveis e eficientes do que as alternativas anteriores como `%` e `.format()`.

## Como é usado neste projeto

F-strings aparecem em todos os arquivos do projeto para exibir resultados ao usuário. Em `codigo_1.py` e `codigo_2.py`, são usadas para mostrar valores monetários com duas casas decimais (`:.2f`). Em `codigo_4.py`, formatam a exibição de cada campo do contato de forma clara e organizada.

## Exemplo do projeto

```python
# codigo_1.py — valor monetário com duas casas decimais
print(f'O valor mensal do plano é de: R$ {valorMensal:.2f}')

# codigo_2.py — interpolação de variável e formatação numérica
print(f'Você pediu uma {nomeSabor} no tamanho {tamanho}: R$ {valor:.2f}\n')

# codigo_4.py — exibição de múltiplos campos de um dicionário
print(f'Id: {contato["Id"]}')
print(f'Nome: {contato["Nome"]}')
print(f'Atividade: {contato["Atividade"]}')
print(f'Telefone: {contato["Telefone"]}')
```

## Recursos para aprofundamento

- [Formatted String Literals – Python Docs](https://docs.python.org/3/reference/lexical_analysis.html#f-strings) — documentação oficial das f-strings
- [Python f-strings – Real Python](https://realpython.com/python-f-strings/) — guia completo com casos de uso avançados e comparação com métodos anteriores
