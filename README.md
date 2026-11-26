# Análise de frota

Com uma amostra fictícia de quatro veículos, o notebook calcula a média de km/L da frota e monta a fila de inspeções de pneus.

A amostra soma **3.015 km** e **1.120 L**, com média de **2,69 km/L**. Na data de referência, 26/11/2026, dois veículos já tinham atingido o prazo de 30 dias e um veículo estava sem registro.

## Como reproduzir

Abra o [notebook](analise_de_frota.ipynb) para ver os dados, os cálculos e a lista de prioridades. Para executar, rode as células em ordem no Jupyter ou no VS Code com Python 3.10 ou superior. Os dados estão no próprio notebook e o código usa a biblioteca padrão.

## Documentação e preventivas

Na rotina de frota, acompanho CIV, CIPP, cronotacógrafo e IPEM, junto com a programação das preventivas. A [base de exemplo em CSV](controle-documentacao-preventivas.csv) reproduz a estrutura do meu controle com uma linha por veículo e dados fictícios.

O saldo da preventiva é a quilometragem da última revisão mais **20.000 km**, menos o hodômetro atual. Com saldo negativo, a preventiva está vencida. Entre **0 e 3.000 km**, entra como prioridade. Para os documentos, o controle sinaliza prazos vencidos e vencimentos em até **30 dias**. Marcações como **FALTANDO**, **CTPP** e **A INFORMAR** ficam como texto e não entram no cálculo de dias.

Na amostra de 25/11/2026, a preventiva do **F-102** tem saldo de **2.800 km** e o CIPP vence em **27 dias**. Os dois entram na programação pela regra do controle.

### Teste no Excel

Abra [baixar-planilha.html](baixar-planilha.html). No GitHub, use **Download raw file** (ícone de download), abra o HTML baixado no navegador e clique em **Baixar planilha (.xlsx)**.

Na aba **Base Editável**, altere o KM atual do F-102 de **218.200** para **217.999**. O saldo passa de **2.800** para **3.001 km** e a preventiva sai da fila de prioridades no **Controle Geral**. Os registros são fictícios.
