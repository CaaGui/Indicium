# Indicium

## Passo 1
Para a utillização do projeto, será necessário a instalação das bibliotecas a seguir:
- Numpy
  pip install numpy
- Pandas
  pip install pandas
- Pycaret
  pip install pycaret[full]

## Passo 2
Após a intalação, abra o python e importe as bibliotecas:
  import numpy as np
  import pandas as pd
  from pycaret.regression import *

## Passo 3
Carregue o modelo de predição:
  modelo = load_model('LH_CD_MODEL_HOUSE_PRICE.pkl')

## Passo 4
O modelo tem como variáveis : host_name, longitude, minimo_noites, ultima_review, disponibilidade_365, bairro e latitude
Crie um pandas DataFrame com as variáveis e seus respectivos valores

## Passo 5
Iniciar o modelo de predição:
  predict = predict_model( modelo, 'pandas DataFrame')
  print('Preço predito $',predict['prediction_label'].values[0].round(2))
