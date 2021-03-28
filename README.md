# Chargemap

endpoint: ` http://my-app.jelastic.metropolia.fi`

## GET 5 stations
endpoint: ` http://my-app.jelastic.metropolia.fi/stations`
## GET location in specific area
 `http://my-app.jelastic.metropolia.fi/stations?topRight={"lat":60.2821946,"lng":25.036108}&bottomLeft={"lat":60.1552076,"lng":24.7816538}`
## GET one station
endpoint:`http://my-app.jelastic.metropolia.fi/stations/5e590b0a7536c009841db2df`
## POST new station
endpoint: ` http://my-app.jelastic.metropolia.fi/stations`
  ```JSON{
    "Station": {
        "Title": "Capgemini Oy",
        "Town": "Espoo",
        "AddressLine1": "Sinimäentie 8b",
        "StateOrProvince": "Southern Finland",
        "Postcode": "02630",
        "Location": {
        "coordinates": [24.77772323548868, 60.203353130088146]
        }
    },
    "Connections":[
        {
        "ConnectionTypeID": "5e39eecac5598269fdad81a0",
        "CurrentTypeID": "5e39ef4a6921476aaf62404a",
        "LevelID": "5e39edf7bb7ae768f05cf2bc",
        "Quantity": 2
        }
    ]
}
````

## PUT modify station
endpoint: ` http://my-app.jelastic.metropolia.fi/stations`
```JSON
 {
        "Station": {
            "_id": "5e8df9a81f87eb168e4c6757",
            "Title": "Modify Station",
            "Town": "Vantaa",
            "AddressLine1": "New address",
            "StateOrProvince": "Southern Finland",
            "Postcode": "02630",
            "Location": {
                "coordinates": [24.77772323548868, 60.203353130088146]
                }
        },
        "Connections":[
                {
                "_id": "5e8df9a81f87eb168e4c6756",
                "ConnectionTypeID": "5e39eecac5598269fdad81a0",
                "CurrentTypeID": "5e39ef4a6921476aaf62404a",
                "LevelID": "5e39edf7bb7ae768f05cf2bc",
                "Quantity": 7
                }
          ]
        }
```



## DELETE
endpoint:`http://my-app.jelastic.metropolia.fi/stations/5e590b0a7536c009841db2df`
