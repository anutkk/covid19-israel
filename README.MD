# How Bad Will Tomorrow Be? Covid Infection Rate Forecast using GRU

A bit of research done with the official [Israeli Covid-19 dataset](https://data.gov.il/dataset/covid-19).

We leverage a small Gated Recurrent Unit (GRU) trained on publicly available data to perform multivariate regression and forecast the short-time spread of the disease in different towns in Israel. The originality of our research lays in extracting short-term features using a small GRU. The model attempts to infers relative intergeographic correlations. 

We find that a GRU has lower prediction error than current state-of-the-art models. Its performance is improved even more when incorporating a simpler model's prediction into the preprocessing stage. However, we find that the deep learning model gives comparable results to state-of-the-art method, and suggest that its potential may be better leveraged by fusing additional sources of data, such as encodings of the social distancing and lockdown regulations.

You may find the complete report at `COVID_GRU_Paper.pdf`. The code is in `Short_Term_Forecast_Using_GRU.ipynb`.


## Bonus: Interactive Map
In the directory `confirmed_place_time` - some (ugly) code which creates a (quite beautiful) interactive map with evolution of confirmed cases by town.

A few interesting pieces of code there - parsing and aggregating the data, and converting new ITM (Israel Tranverse Mercator - רשת ישראל החדשה) to normal WGS84 geographical coordinates.