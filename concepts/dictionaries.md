# Dicionários (Dictionaries)

## O que é

Um dicionário em Python é uma estrutura de dados que armazena pares de **chave-valor**. Ao contrário de listas, que usam índices numéricos, os dicionários permitem acessar valores por chaves com semântica descritiva — como `contato['Nome']` em vez de `contato[1]`. São definidos com chaves `{}` e os pares são separados por vírgula.

Dicionários são mutáveis (podem ser alterados após a criação), não ordenados por inserção até o Python 3.6 e ordenados a partir do Python 3.7. São ideais para representar **objetos simples com atributos nomeados**, como registros de contatos, configurações ou respostas de APIs. O método `.copy()` cria uma cópia independente do dicionário, evitando que alterações posteriores afetem o original.

## Como é usado neste projeto

Em `codigo_4.py`, cada contato da agenda é representado como um dicionário com as chaves `'Id'`, `'Nome'`, `'Atividade'` e `'Telefone'`. A função `cadastrar_contato()` cria um dicionário vazio, preenche os campos com as entradas do usuário e o adiciona à `lista_contatos` com `.append(contato.copy())`. A busca por parâmetro em `consultar_por_parametro()` compara o valor de uma chave específica para filtrar contatos.

## Exemplo do projeto

```python
# codigo_4.py — criação e preenchimento de um dicionário de contato
def cadastrar_contato(id):
    contato = {}
    contato['Id'] = id
    contato['Nome'] = input('Por favor entre com o nome do Contato: ')
    contato['Atividade'] = input('Por favor entre com a Atividade do contato: ')
    contato['Telefone'] = input('Por favor entre com o telefone do contato: ')
    lista_contatos.append(contato.copy())  # .copy() evita referência ao mesmo objeto

# Acesso por chave na listagem
for contato in lista_contatos:
    print(f'Id: {contato["Id"]}')
    print(f'Nome: {contato["Nome"]}')
```

## Recursos para aprofundamento

- [Dictionaries – Python Docs](https://docs.python.org/3/tutorial/datastructures.html#dictionaries) — documentação oficial sobre dicionários em Python
- [Python Dictionaries – Real Python](https://realpython.com/python-dicts/) — guia completo com operações, métodos e boas práticas
