## Indice
- [Introduzione](#introduzione)
- [Come usare l'applicazione](#come-usare-lapplicazione)
- [Rotte](#rotte)
   - [localhost:80/citiesWeather](#localhost80citiesWeather)
   - [localhost:80/citiesForecast](#localhost80citiesForecast)
- [Strumenti utilizzati](#strumenti-utilizzati)
- [Autori](#autori)

## Introduzione
Questo progetto si pone l'obiettivo di creare una applicazione Java che, tramite un Client come Postman, permetta all’utente di selezionare più città e confrontare in contemporanea le informazioni metereologiche. L’utente potrà visualizzare le previsioni correnti e future delle città, avendo la possibilità di integrare dei filtri, per selezionare fascie orarie specifiche o avere statistiche riguardanti i valori minimi, massimi, media e varianza delle varie misurazioni. 

## Come usare l'applicazione
Per utilizzare questa applicazione si deve procedere clonando questa repository sul pc e importando nell’IDE Eclipse il progetto PavicSasuProgettoJava. Una volta aperto Eclipse, per avviare il programma, basta selezionare PavicSasuProgettoJava nel proprio package explorer e dare il comando Run as -> Spring Boot App (all’avvio comparirà il logo di Spring). L’applicativo permetterà di visualizzare le varie informazioni metereologiche collegandosi alle rotte (elencate successivamente) sulla rete interna all’indirizzo localhost, sulla porta 80.

## Rotte
| Metodo | Rotta | Descrizione |
|:--------------|:-------------:|:--------------|
| POST | /citiesWeather | Ottiene la previsione attuale di tutte le città scelte|
| POST | /citiesForecast | Ottiene la previsione futura delle città scelte con la possibilità di integrare filtri e statistiche |

### localhost:80/citiesWeather
L’API deve essere richiamata con il metodo HTTP POST e il body deve avere un oggetto JSON di questo tipo:
```json
{
    "cities" : ["Rome,IT" , "Berlin,DE"]
}
```
Per le previsioni correnti si ottiene il seguente JSON:
```json
{
    "Rome,IT": [
        {
            "date": "2022-01-19T10:16:16.000+00:00",
            "cloud": 40.0,
            "visibility": 10000.0,
            "temperature": 9.63,
            "humidity": 69.0,
            "pressure": 1031.0
        }
    ],
    "Berlin,DE": [
        {
            "date": "2022-01-19T10:08:52.000+00:00",
            "cloud": 40.0,
            "visibility": 10000.0,
            "temperature": 4.49,
            "humidity": 83.0,
            "pressure": 1020.0
        }
    ]
}


