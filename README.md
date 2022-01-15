# Pràctica Kaggle APC UAB 2021-22
### Nom: ***** Rubén Gasque
### DATASET: *****
### URL: [kaggle](https://www.kaggle.com/benfattori/league-of-legends-diamond-games-first-15-minutes/tasks?taskId=154)
## Resum
El dataset tracta dades obtingudes en els primers 15 minuts d'una partida del league of legends. En total tenim 19 atributs i 48651 files.

Entre els atributs més destacats trobem l'or obtingut per cada equip, els minions i enemics assasinats, torres enemigues enderrocades, entre d'altres.

La majoria d'aquestes dades són de tipus float tot i que també tenim unes poques de tipus enter. L'atribut que nosaltres hem agafat com objectiu es blue_win que representa si l'equip blau guanya o no (binàriament amb 1 o 0 segons victòria o derrota), que és l'atribut sobre el qual farem la nostre classificació.
### Objectius del dataset
El nostre objectiu és tractar de predir la victòria d'un equip o de l'altre només tenint les dades dels primers 15 minuts de partida. Per fer-ho aplicarem diversos models de classificació per veure si podem conseguir trobar un model que classifiqui correctament les dades.
### Preprocessat
Abans d'entrenar el model hem hagut d'estudiar les dades i ens hem adonat que hi havien uns quants atributs que no ens servien de cara a la classificació ja que no ens aportaven cap mena d'informació útil. 

També hi havien 2 atributs que representaven la quantitat de dracs assasinats que hem vist com eren errònis ja que tots els seus valors eren 0 i els hagut d'eliminar.
### Model
| Decision Tree | criterion='entropy', max_depth=6, splitter='best' | Score: 77.44 % | 
| KNN | n_neighbors=10, weights='uniform', metric='manhattan' | Score: 75.25 % | 

## Conclusions
El millor model que s'ha aconseguit ha estat el decision tree. 
El model knn també ha classificat força bé amb un accuracy bo però tot i no ser molt millor, el decision tree ha classificat de millor manera les dades tenint menys errers i un score major.
## Idees per treballar en un futur
En un futur es podria provar d'aplicar més models per veure si algún millora els provats en aquest treball, com per exemple el svc, un regressor logístic o un k-means.

