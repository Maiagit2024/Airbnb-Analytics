🏡 Análise de Dados Airbnb - Rio de Janeiro





📘 Índice

🚀 Visão Geral

✨ Funcionalidades

🛠 Tecnologias Utilizadas

🗂 Estrutura do Repositório

🔧 Instalação e Execução

📊 Pipeline ETL

📈 Dashboard Power BI

🤝 Contribuição

✉️ Contato

⚖️ Licença

🚀 Visão Geral

Este projeto apresenta uma análise completa dos anúncios do Airbnb no Rio de Janeiro (2020–2024), visando gerar insights para cenários de turismo e investimento imobiliário. Através de um pipeline ETL em Python e visualizações interativas no Power BI, você poderá:

Explorar padrões de disponibilidade e ocupação anual.

Comparar preços médios por tipo de quarto e por bairro.

Avaliar tendências de avaliação de hóspedes ao longo dos últimos 5 anos.

✨ Funcionalidades

Tratamento de Dados: limpeza e padronização de valores faltantes (reviews, quartos, notas).

Enriquecimento Geoespacial: mapeamento de latitude/longitude para bairros exatos.

Métricas Avançadas:

Disponibilidade anual (availability_365).

Ocupação estimada como fração do ano.

Preço médio geral e por tipo de quarto.

Análise de reviews mensais.

Dashboard Interativo: filtros por ano, bairro e tipo de quarto.

🛠 Tecnologias Utilizadas

Python (Google Colab)

pandas, geopandas, numpy

Power BI Desktop

Dados

Kaggle: anúncios Airbnb RJ

Data.Rio: mapa de bairros (shapefile)

🗂 Estrutura do Repositório

├── assets/                 # Imagens, banners e GIFs
│   └── airbnb_dashboard.gif
├── data/                   # Dados brutos e processados
│   ├── listings_com_bairro_exato.csv

             # ETL em Python
├── shapefiles/             # Dados geoespaciais
│   └── bairros_rj.shp
├── powerbi/                # Arquivos .pbix e tema customizado
│   ├── dashboard_airbnb.pbix
│   └── theme_airbnb.json
└── README.md               # Documentação do projeto

🔧 Instalação e Execução

Pré-requisitos

Python 3.8+ instalado

Power BI Desktop

Configurar ambiente Python

pip install -r requirements.txt

ETL no Google Colab

Abra notebooks/01_etl_airbnb.ipynb no Colab

Execute as células para gerar data/airbnb_clean.csv

Dashboard

Abra powerbi/dashboard_airbnb.pbix no Power BI

Desfrute das visualizações!

📊 Pipeline ETL

Extração: importação do CSV original do Kaggle.

Transformação:

Substituição de NaN por 0 em number_of_reviews e reviews_per_month.

Conversão de tipos de dados (strings → floats).

Limpeza de espaços nulos/"desconhecido" em bairros.

Preenchimento de notas faltantes (review_scores_rating).

Enriquecimento:

Uso de geopandas para associar coordenadas a bairros exatos.

Carregamento: exportação para CSV e conexão Power BI.

📈 Dashboard Power BI

Veja o GIF abaixo para um preview do dashboard:

Principais visuais:

Linha do tempo de avaliações (2020–2024)

Histograma de disponibilidade anual

Mapa geoespacial com anúncios por bairro

Cartões de métricas: preço médio, ocupação, total de anúncios

✉️ Contato

José Maia – https://www.linkedin.com/in/josé-maia-ju0ni8 - LinkedIn 
