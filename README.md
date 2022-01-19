## Indice
- [Introduzione](#introduzione)
- [Come usare l'applicazione](#come-usare-l'applicazione)
- [Rotte](#rotte)
   - [localhost:80/citiesWeather](#citiesWeather)
   - [localhost:80/citiesForecast](#citiesForecast)
- [Strumenti utilizzati](#strumenti-utilizzati)
- [Autori](#autori)

## Introduzione
Questo progetto si pone l'obiettivo di creare una applicazione Java che, tramite un Client come Postman, permetta all’utente di selezionare più città e confrontare in contemporanea le informazioni metereologiche. L’utente potrà visualizzare le previsioni correnti e future delle città, avendo la possibilità di integrare dei filtri, per selezionare fascie orarie specifiche o avere statistiche riguardanti i valori minimi, massimi, media e varianza delle varie misurazioni. 

```json
{
    "cities" : ["Rome,IT" , "Berlin,DE"] ,
    "days" : 2 ,   
    "interval" : "10:00->16:00" ,
    "stats" : true
}
```
| Headline 1 in the tablehead | Headline 2 in the tablehead | Headline 3 in the tablehead |
|:--------------|:-------------:|--------------:|
