# Classificação de Aves com Árvore de Decisão

Este projeto consiste em um modelo de machine learning desenvolvido como atividade acadêmica, com o objetivo de estudos. Consiste em classificar aves em três categorias: **Ave Carnívora**, **Ave Herbívora** e **Ave Onívora**. A classificação é feita com base em características específicas de cada ave.

## Descrição do Projeto

A pesquisa utiliza um **modelo de Árvore de Decisão** para classificar aves de acordo com três características coletadas:
- **Envergadura das asas** (em cm)
- **Peso** (em kg)
- **Comprimento do bico** (em cm)

Com esses dados, o modelo é treinado para identificar o tipo de alimentação da ave.

### Categorias de Aves
1. **Ave Carnívora**
2. **Ave Herbívora**
3. **Ave Onívora**

## Dados de Treinamento

Os dados de treinamento foram coletados e incluem três amostras com as características e a categoria correspondente:

| Envergadura das Asas (cm) | Peso (kg) | Comprimento do Bico (cm) | Categoria         |
|---------------------------|-----------|--------------------------|-------------------|
| 120                       | 3.5       | 7                        | Ave Carnívora     |
| 85                        | 1.2       | 4                        | Ave Herbívora     |
| 95                        | 2.1       | 6                        | Ave Onívora       |

Essas amostras são utilizadas para treinar o modelo de árvore de decisão, que então será capaz de classificar novas aves com base em características similares.

## Implementação do Modelo

O modelo é desenvolvido em Python utilizando a biblioteca `scikit-learn`. Abaixo está um exemplo de código para treinar o modelo e classificar uma nova ave.

### Exemplo de Código

```python
from sklearn.tree import DecisionTreeClassifier

# Dados de treinamento
treino = [
    [120, 3.5, 7],  # Ave Carnívora
    [85, 1.2, 4],   # Ave Herbívora
    [95, 2.1, 6]    # Ave Onívora
]
resposta = ['Ave Carnívora', 'Ave Herbívora', 'Ave Onívora']

# Criação do modelo de Árvore de Decisão
modelo = DecisionTreeClassifier()

# Treinamento do modelo
modelo.fit(treino, resposta)

# Dados de teste
teste = [
    [90, 1.5, 5]  # Ave de teste
]

# Classificação da ave de teste
classificacao = modelo.predict(teste)

# Exibição da categoria atribuída à ave de teste
print('Categoria da ave de teste:', classificacao[0])

```

## Teste do Modelo

Após o treinamento, o modelo é testado com uma nova ave com as características a seguir:

- **Envergadura das asas:** 90 cm
- **Peso:** 1.5 kg
- **Comprimento do bico:** 5 cm

## Resultado
O modelo classifica a ave de teste em uma das três categorias com base nas características fornecidas.

## Dependências

- Python 3.6+
- scikit-learn - instalável com:
```
  pip install scikit-learn
```

## Conclusão

Este projeto demonstra como um modelo de Árvore de Decisão pode ser aplicado na classificação de aves, ajudando pesquisadores a identificar a dieta provável de diferentes espécies com base em suas características físicas.

Feito com ❤️.



