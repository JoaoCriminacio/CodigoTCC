# Estudo sobre Assimetria Informacional em Apostas Esportivas
Este repositório contém o desenvolvimento técnico de uma pesquisa sobre a assimetria informacional em plataformas de apostas esportivas, focando em como os modelos estatísticos das casas de apostas estruturam o favorecimento da banca. A análise utiliza dados históricos do Campeonato Brasileiro (Série A) entre 2012 e 2025.

## 📋 Sobre o Projeto
O objetivo principal é calcular a "odd justa" através de modelos probabilísticos e compará-las com as cotações oferecidas por grandes operadoras. Dessa forma, através de métricas de calibração e precisão, o projeto identifica se as probabilidades implícitas nas odds das casas refletem a realidade estatística ou se apresentam vieses favoráveis ao lucro sistêmico da banca.

## 📊 Modelos Estatísticos Implementados
O repositório inclui a implementação de quatro modelos principais:
- **Modelo de Poisson**: Utiliza a distribuição de Poisson para calcular a probabilidade de gols como eventos independentes e raros baseados em médias históricas (λ).
- **Dixon-Coles**: Uma extensão do modelo de Poisson que incorpora parâmetros de ataque (α) e defesa (β) para cada equipe, ajuste de vantagem em casa (γ) e uma correção de dependência (ρ) para placares baixos e empates.
- **Dixon-Coles com Decaimento Temporal**: Aplica uma função de peso exponencial (ϕ(t)=e −ξt) para dar maior relevância estatística a jogos recentes em detrimento de partidas antigas.
- **Elo Rating**: Sistema de ranqueamento que ajusta a pontuação dos times após cada partida com base na diferença entre o resultado real e o esperado

## 📈 Métricas de Avaliação
Para validar a precisão dos modelos e identificar a assimetria, foram utilizadas as seguintes métricas:
- **Teste Qui-Quadrado (X²)**: Verifica se a distribuição observada dos resultados difere significativamente da distribuição esperada pelas odds.
- **Diferença Percentual Média (DPM)**: Mede a variação relativa entre as probabilidades dos modelos e as probabilidades implícitas das casas.
- **Brier Score**: Quantifica o erro das previsões probabilísticas em uma escala de 0 (perfeito) a 1 (totalmente errado).
- **Curvas de Confiabilidade (Calibração)**: Análise visual que plota a frequência real dos eventos contra a probabilidade prevista para identificar superestimação ou subestimação de chances.

## 🛠️ Tecnologias Utilizadas
- Linguagem: Python
- Ambiente: Jupyter Notebook / Google Colab
- Bibliotecas: Pandas, Numpy, Scipy (stats), Scikit-learn (metrics/calibration), Matplotlib, Seaborn.
- Fontes de Dados: [Football-Data.co.uk](https://football-data.co.uk/) e [OddsAgora](https://www.oddsagora.com.br/).
