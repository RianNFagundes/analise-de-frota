# Análise de frota

Demonstração em Python que consolida consumo de combustível por veículo e organiza a fila de inspeções de pneus. Todos os dados são fictícios.

## Resultados da amostra

| Indicador | Resultado |
| --- | ---: |
| Veículos analisados | 4 |
| Distância total | 3.015 km |
| Consumo total | 1.120 L |
| Eficiência da frota | 2,69 km/L |
| Inspeções vencidas na data de referência | 2 |
| Veículos sem registro de inspeção | 1 |

O notebook calcula km/L a partir dos totais de quilômetros e litros. Para as inspeções, usa um prazo de 30 dias como premissa da demonstração e coloca os veículos sem registro no início da lista.

## Como consultar ou executar

Abra o [notebook de análise](analise_de_frota.ipynb) para ver os cálculos, os resultados e a leitura dos indicadores. Para reproduzir, execute as células em ordem no Jupyter ou no VS Code com Python 3.10 ou superior. Os dados estão no próprio notebook, e a análise usa apenas a biblioteca padrão do Python.
