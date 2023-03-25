# COVID 19 API (from WHO data) 

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

## Features:

- Provide cases, deaths, recovered and fatality rate. 
- Two type data: by world and by countries.
- Also provide data origin from WHO

## Usage:
### 1. Get covid 19 data overview (world)
- dataFormat: Data is formatted to be easily used.
- dataOrigin: Data without formatting and get it directly from the WHO website.

API: [https://covid19-merlin.vercel.app/api/world](https://covid19-merlin.vercel.app/api/world)

#### Example:
```sh
{
    dataFormat: {
        "Confirmed": 761071826,
        "Deaths": 6879677,
        "Recovered": 754192149,
        "Fatality_Rate": 0.9
    },
    dataOrigin": {
        startDate: {
          "date": "2020-01-03T00:00:00.000Z"
        },
        today: {
          "Confirmed": 33950,
          "Cumulative_Confirmed": 761071826,
          "Cumulative_Deaths": 6879677,
          "Deaths": 198
        },
        totals: {
          "Avg7Case": 760835532.302058,
          "Avg7CasePop": 4758814.299999877,
          "Avg7Death": 6878075.49800127,
          "Avg7DeathPop": 23850.199999999204,
          "Cases_Last_7_Days": 5325809808,
          "Cases_Last_7_Days_Change": 8616467.82999984,
          "Cases_Per_Hundred_Thousand": 2099492668.3189237,
          "Confirmed": 761071826,
          "Cumulative_Confirmed": 331038930687,
          "Cumulative_Deaths": 4498882227,
          "Deaths": 6879677,
          "Deaths_Last_7_Days": 48145569,
          "Deaths_Last_7_Days_Change": 3646441.610000062,
          "Deaths_Per_Hundred_Thousand": 17945935.386000104,
          "WkCasePop": 33381261.879000094,
          "WkDeathPop": 204494.71099999917
        }
    }
}
```

### 2. Get covid 19 data by countries

- dataFormat: Data is formatted to be easily used.
- dataOrigin: Data without formatting and get it directly from the WHO website.

API:  [https://covid19-merlin.vercel.app/api/countries](https://covid19-merlin.vercel.app/api/countries)

#### Example:

```sh
{
    dataFormat: [
        {
          "CountryCode": "US",
          "CountryName": "United States of America",
          "Confirmed": 102544598,
          "Deaths": 1114970,
          "Recovered": 101429628,
          "Fatality_Rate": 1.09
        },
        {
          "CountryCode": "CN",
          "CountryName": "China",
          "Confirmed": 99229372,
          "Deaths": 120775,
          "Recovered": 99108597,
          "Fatality_Rate": 0.12
        },
        ...
        {
          "CountryCode": "TM",
          "CountryName": "Turkmenistan",
          "Confirmed": 0,
          "Deaths": 0,
          "Recovered": 0,
          "Fatality_Rate": null
        }
    ],
    dataOrigin: [
        {
          "Country": "US",
          "Deaths": 1114970,
          "Cumulative Deaths": 724018110,
          "Deaths Last 7 Days": 1741,
          "Deaths Last 7 Days Change": -7.74,
          "Deaths Per Hundred Thousand": 336.846,
          "Confirmed": 102544598,
          "Cumulative Confirmed": 54277782366,
          "Cases Last 7 Days": 126613,
          "Cases Last 7 Days Change": -25.78,
          "Cases Per Hundred Thousand": 30979.993,
          "WkCasePop": 216745.17000000013,
          "WkDeathPop": 2356.3400000000042,
          "Avg7Case": 102490335.26599959,
          "Avg7Death": 1114223.8500000006,
          "Avg7CasePop": 30909.20000000004,
          "Avg7DeathPop": 283.4000000000062,
          "coords": {
            "latitude": 38,
            "longitude": -97
            },
          "name": "United States of America",
          "Cases Last 24 hours": 0,
          "Deaths Last 24 hours": 0,
          "Doses Per 100": 200.82,
          "Persons Vaccinated Per 100": 80.588,
          "Persons fully vaccinated with last dose of primary series": 68.717,
          "First Vaccine Date": "2020-12-14",
          "Total Doses Administered": 664718300,
          "Persons Vaccinated": 266747359,
          "Persons Fully Vaccinated": 227456203,
          "Latest Measures": {
            "ISO_2_CODE": "US",
            "DATE_START": "2022-12-31",
            "WHO_REGION": "AMRO",
            "COUNTRY": "United States of America",
            "MASKS": 50,
            "TRAVEL": 33,
            "GATHERINGS": 0,
            "SCHOOLS": 17,
            "BUSINESSES": 17,
            "MOVEMENTS": 33,
            "GLOBAL_INDEX": 25
          },
          "Persons Received Booster or Additional Dose": 115817663,
          "Boosters per 100": 34.99
        },
        ...
        {
          "Country": "TM",
          "Deaths": 0,
          "Cumulative Deaths": 0,
          "Deaths Last 7 Days": 0,
          "Deaths Last 7 Days Change": 0,
          "Deaths Per Hundred Thousand": 0,
          "Confirmed": 0,
          "Cumulative Confirmed": 0,
          "Cases Last 7 Days": 0,
          "Cases Last 7 Days Change": 0,
          "Cases Per Hundred Thousand": 0,
          "WkCasePop": 0,
          "WkDeathPop": 0,
          "Avg7Case": 0,
          "Avg7Death": 0,
          "Avg7CasePop": 0,
          "Avg7DeathPop": 0,
          "coords": {
            "latitude": 40,
            "longitude": 60
          },
          "name": "Turkmenistan",
          "Cases Last 24 hours": 0,
          "Deaths Last 24 hours": 0,
          "Doses Per 100": 216.2,
          "Persons Vaccinated Per 100": 55.702,
          "Persons fully vaccinated with last dose of primary series": 55.684,
          "First Vaccine Date": "2021-02-24",
          "Total Doses Administered": 13040514,
          "Persons Vaccinated": 3359468,
          "Persons Fully Vaccinated": 3358426,
          "Latest Measures": {
            "ISO_2_CODE": "TM",
            "DATE_START": "2022-12-31",
            "WHO_REGION": "EURO",
            "COUNTRY": "Turkmenistan",
            "MASKS": 0,
            "TRAVEL": 33,
            "GATHERINGS": 0,
            "SCHOOLS": 0,
            "BUSINESSES": 0,
            "MOVEMENTS": 0,
            "GLOBAL_INDEX": 6
          },
          "Persons Received Booster or Additional Dose": 3171535,
          "Boosters per 100": 52.586
        }
    ]
}
```

## References:

- Website: [https://covid19.who.int/table](https://covid19.who.int/table)
- API (first): [https://covid19.who.int/page-data/index/page-data.json](https://covid19.who.int/page-data/index/page-data.json)
- API (second): [https://covid19.who.int/page-data/sq/d/3713876948.json](https://covid19.who.int/page-data/sq/d/3713876948.json)

## License:
MIT

## Author:

Merlin Le (Lê Trường Thịnh)

 

   
