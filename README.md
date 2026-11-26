# Análise de frota

Com uma amostra fictícia de quatro veículos, o notebook calcula a média de km/L da frota e monta a fila de inspeções de pneus.

A amostra soma **3.015 km** e **1.120 L**, com média de **2,69 km/L**. Na data de referência, 26/11/2026, dois veículos já tinham atingido o prazo de 30 dias e um veículo estava sem registro.

## Como reproduzir

Abra o [notebook](analise_de_frota.ipynb) para ver os dados, os cálculos e a lista de prioridades. Para executar, rode as células em ordem no Jupyter ou no VS Code com Python 3.10 ou superior. Os dados estão no próprio notebook e o código usa a biblioteca padrão.

## Documentação e preventivas

Na rotina de frota, acompanho os vencimentos de CIV, CIPP, cronotacógrafo (CRONO) e IPEM e a programação de manutenção preventiva. A [base de exemplo em CSV](controle-documentacao-preventivas.csv) mostra como esses itens podem entrar no mesmo controle. Os veículos, datas e quilometragens da amostra são fictícios.

Na demonstração, o item entra na programação quando faltam até 15 dias ou 1.000 km para o limite. Por exemplo, a preventiva do F-101 aparece como **A programar** porque faltam 500 km, embora o vencimento por data esteja a 34 dias. A amostra também separa os itens vencidos dos registros que precisam de prazo ou hodômetro.
