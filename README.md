# London Bike Sharing

## Índice

- [Introdução](#1-introdução)
- [Como Usar](#2-como-usar)
- [Descrição dos Dados](#3-descrição-dos-dados)
- [Tecnologias Usadas](#4-tecnologias-usadas)

## 1. Introdução

O projeto analisa dados de compartilhamento de bicicletas em Londres. O conjunto de dados mostra a quantidade de bicicletas alugadas a cada hora e parâmetros relacionados, como temperatura, umidade e velocidade do vento. 

O conjunto de dados foi obtido através do Kaggle e está disponível no seguinte link: [London Bike Sharing Dataset](https://www.kaggle.com/datasets/hmavrodiev/london-bike-sharing-dataset).

## 2. Como Usar

Para iniciar o projeto, siga os passos abaixo:

1. **Instale as dependências:**

   ```bash
    pip install -r requirements.txt
    ```

2. **Prepare os Dados:**

    - O arquivo [01_extract_files.ipynb](01_extract_files.ipynb) é utilizado para fazer o download e extrair o arquivo .zip do Kaggle. 

    - Ambos os arquivos, o .zip e os arquivos extraídos, serão armazenados na pasta [datasets](./datasets/).

3. **Análise Exploratória:**

    - Use o notebook [02_london_bikes.ipynb](02_london_bikes.ipynb) para realizar a limpeza e análise exploratória dos dados. 

    - Após a análise, um arquivo Excel chamado [london_bikes_final.xlsx](./datasets/london_bikes_final.xlsx) será gerado e salvo na pasta [datasets](./datasets/).

4. **Dashboard:**

    - Um dashboard foi criado no Tableau com os dados limpos e está disponível no seguinte link: [London Bike Rides Dashboard](https://public.tableau.com/app/profile/pedro.sancho/viz/LondonBikeRides_17217390531790/Dashboard).

    - O arquivo [London_bike_ride.twb](./dashboard/London_bike_ride.twb) foi salvo na pasta [dashboard](./dashboard/), caso queira importar o projeto no Tableau

## 3. Descrição dos Dados

O conjunto de dados inclui as seguintes colunas:

- `timestamp`: Data e hora para agrupamento dos dados.
- `cnt`: Contagem de novas bicicletas compartilhadas.
- `t1`: Temperatura real em °C.
- `t2`: Temperatura em °C que "se sente como".
- `hum`: Umidade em porcentagem.
- `windspeed`: Velocidade do vento em km/h.
- `weather_code`: Categoria do clima.
- `is_holiday`: Campo booleano - 1 se for feriado / 0 se não for.
- `is_weekend`: Campo booleano - 1 se o dia for um final de semana.
- `season`: Categoria dos meteorológicos das estações:
    - 0 = spring; 
    - 1 = summer; 
    - 2 = fall; 
    - 3 = winter.

- `weather_code`: descrição das condições climáticas
    - 1 = Clear ; mostly clear but have some values with haze/fog/patches of fog/ fog in vicinity 
    - 2 = scattered clouds / few clouds 
    - 3 = Broken clouds 
    - 4 = Cloudy 
    - 7 = Rain/ light Rain shower/ Light rain 
    - 10 = rain with thunderstorm 
    - 26 = snowfall 
    - 94 = Freezing Fog

## 4. Tecnologias Usadas

- `Python`: Linguagem de programação principal.
- `Jupyter Notebook`: Para análise e limpeza dos dados.
- `Pandas`: Biblioteca para manipulação e análise de dados.
- `Tableau`: Para criação do dashboard.
