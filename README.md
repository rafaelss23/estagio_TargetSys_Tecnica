# Resolução do Desafios Técnicos em Python

Este repositório contém a resolução e descrição do código em Python

## 1. Cálculo da Soma de uma Sequência

### Descrição

Dado o trecho de código abaixo:

```python
int INDICE = 13, SOMA = 0, K = 0;
Enquanto K < INDICE faça {
    K = K + 1;
    SOMA = SOMA + K;
}
Imprimir(SOMA);
```
### Resultado: `91` 


## 2. Verificação de Número na Sequência de Fibonacci

### Descrição

Dado um número, o programa deve calcular a sequência de Fibonacci e retornar uma mensagem indicando se o número informado pertence ou não à sequência.

```python
def is_fibonacci(n):
    if n < 0:
        return False
    
    a, b = 0, 1
    
    while a <= n:
        if a == n:
            return True
        a, b =
```
### Resultado: `O número 21 pertence à sequência de Fibonacci.` 

## 3. Análise de Faturamento Diário de uma Distribuidora

### Descrição

Dado um vetor que guarda o valor de faturamento diário de uma distribuidora, o programa deve calcular:

O menor valor de faturamento ocorrido em um dia do mês;
O maior valor de faturamento ocorrido em um dia do mês;
O número de dias no mês em que o valor de faturamento diário foi superior à média mensal.
O código em Python é:

```python

import json

faturamento_json = """
[
    {"dia": 1, "valor": 22174.1664},
    {"dia": 2, "valor": 24537.6698},
    {"dia": 3, "valor": 26139.6134},
    {"dia": 4, "valor": 0.0},
    {"dia": 5, "valor": 0.0},
    {"dia": 6, "valor": 26742.6612},
    {"dia": 7, "valor": 0.0},
    {"dia": 8, "valor": 42889.2258},
    {"dia": 9, "valor": 46251.174},
    {"dia": 10, "valor": 11191.4722}
]
"""

faturamento = json.loads(faturamento_json)

valores = [dia["valor"] for dia in faturamento if dia["valor"] > 0]

menor_valor = min(valores)
maior_valor = max(valores)
media_mensal = sum(valores) / len(valores)

dias_acima_da_media = sum(1 for valor in valores if valor > media_mensal)

print(f"Menor valor de faturamento: {menor_valor:.2f}")
print(f"Maior valor de faturamento: {maior_valor:.2f}")
print(f"Dias com faturamento acima da média: {dias_acima_da_media}")
```

### Resultado:</br> `Menor valor de faturamento: 11191.47`</br> `Maior valor de faturamento: 46251.17`</br> `Dias com faturamento acima da média: 2`
 

## 4. Percentual de faturamento por estado 
### Descrição
- SP – R$67.836,43
- RJ – R$36.678,66
- MG – R$29.229,88
- ES – R$27.165,48
- Outros – R$19.849,53

<b>Escreva um programa na linguagem que desejar onde calcule o percentual de representação que cada estado teve dentro do valor total mensal da distribuidora.</b>

```python
faturamento_estados = {
    "SP": 67836.43,
    "RJ": 36678.66,
    "MG": 29229.88,
    "ES": 27165.48,
    "Outros": 19849.53
}

faturamento_total = sum(faturamento_estados.values())

for estado, valor in faturamento_estados.items():
    percentual = (valor / faturamento_total) * 100
    print(f"{estado}: {percentual:.2f}%")
```

### Resultado:</br> `SP: 37.53%`</br> `RJ: 20.29%` </br> `MG: 16.17%` </br> `ES: 15.03%` </br> `Outros: 10.98%` 

## 5) Escreva um programa que inverta os caracteres de um string. <br>

<i>IMPORTANTE:</i>
<b>a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;</b><br>
<b>b) Evite usar funções prontas, como, por exemplo, reverse;</b>


```python
def inverte_string(s):
    invertida = ""
    for char in s:
        invertida = char + invertida
    return invertida

# Exemplo de uso:
string_exemplo = "Exemplo"
print(inverte_string(string_exemplo))
```

### Resultado: `olpmexE` 



