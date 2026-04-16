<div align="center">

# Trabalho — Lógica de Programação e Algoritmos

Quatro desafios práticos em Python desenvolvidos para a disciplina de Lógica de Programação e Algoritmos.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Language](https://img.shields.io/badge/Python-3.6+-3776AB.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

</div>

---

## 📋 Sobre

Este projeto reúne quatro programas Python desenvolvidos como trabalho da disciplina **Lógica de Programação e Algoritmos** do curso de Análise e Desenvolvimento de Sistemas (UNINTER). Cada desafio aplica conceitos fundamentais de programação como funções, estruturas condicionais, laços de repetição, tratamento de exceções e manipulação de dados.

## 🚀 Tecnologias

- **Python 3.6+** — linguagem principal, com uso de f-strings e dicionários
- **Módulos built-in** — apenas recursos nativos do Python (sem dependências externas)

## 📁 Estrutura do projeto

```
trabalho-logica-programacao/
├── codigo_1.py     ← Plano de saúde: cálculo de valor mensal por faixa etária
├── codigo_2.py     ← Pizzaria: pedidos múltiplos com acumulador e cardápio
├── codigo_3.py     ← Madeireira: cálculo de custo com desconto por volume e transporte
├── codigo_4.py     ← Agenda de contatos: CRUD em memória com menus interativos
├── concepts/       ← documentação de conceitos de programação
├── README.md
└── LICENSE
```

## ⚙️ Como executar

Não há dependências externas. Basta ter Python 3.6 ou superior instalado.

```bash
# Clone o repositório
git clone https://github.com/GisellePegado/trabalho-logica-programacao.git
cd trabalho-logica-programacao

# Execute qualquer um dos desafios
python codigo_1.py
python codigo_2.py
python codigo_3.py
python codigo_4.py
```

## 📝 Descrição dos desafios

| Arquivo | Desafio | Destaques |
|---------|---------|-----------|
| `codigo_1.py` | **Plano de Saúde** — calcula o valor mensal de acordo com a faixa etária do cliente | Funções, condicionais encadeadas |
| `codigo_2.py` | **Pizzaria** — sistema de pedidos com cardápio, múltiplos itens e acumulador de total | Loop de pedidos, validação de entrada |
| `codigo_3.py` | **Madeireira** — calcula custo total de toras com desconto por volume e tipo de transporte | Retorno múltiplo, try/except, desconto progressivo |
| `codigo_4.py` | **Agenda de Contatos** — CRUD completo em memória com menus genéricos e busca por parâmetro | Dicionários, listas, funções reutilizáveis |

## 📚 Conceitos explorados

Este projeto utiliza os seguintes conceitos de lógica de programação e Python, documentados na pasta [`concepts/`](concepts/):

| Conceito | Descrição resumida |
|----------|--------------------|
| [Funções](concepts/functions.md) | Blocos reutilizáveis que encapsulam lógica específica em cada desafio |
| [Estruturas Condicionais](concepts/conditional-statements.md) | `if/elif/else` para regras de negócio como faixas etárias e tipos de produto |
| [Laços de Repetição](concepts/loops.md) | `while` e `for` para pedidos repetidos, menus e iteração sobre listas |
| [Validação de Entrada](concepts/input-validation.md) | Padrão `while + try/except` para garantir entradas válidas do usuário |
| [Tratamento de Exceções](concepts/exception-handling.md) | `try/except ValueError` para capturar entradas inválidas sem travar o programa |
| [Dicionários](concepts/dictionaries.md) | Estrutura chave-valor para representar contatos na agenda |
| [Retorno Múltiplo](concepts/multiple-return-values.md) | Função retorna quantidade e desconto simultaneamente via tupla |
| [f-strings](concepts/f-strings.md) | Formatação moderna de strings com interpolação e controle de casas decimais |

> Os arquivos de conceito contêm explicações detalhadas e exemplos extraídos do código.

## 🤝 Contribuindo

Contribuições são bem-vindas! Abra uma issue ou envie um pull request.

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
