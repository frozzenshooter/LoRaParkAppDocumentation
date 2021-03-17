# Sensor List GET /sensors
```json
[
	{
		"id": "davis-013d4d",
		"name": "Weather Station",
		"description": "",
		"domain": ["dom1", "dom2"],
		"location": {
				"latitude": 48.396426,
				"longitude": 9.990453
		}
	}
]
```

# Sensor Details GET /sensor/{sensorID}/details(/{lang})
```json
[
	{
		"name": "Wetterstation: Temperatur",
		"value": "JAA",
		"unit": "°C",
		"timestamp": ""
	},
	{
		"name": "Temperatur",
		"value": "1000",
		"unit": "°F",
		"timestamp": ""
	}
]
```

# Sensor Raw Values GET /sensors/raw?id={sensorID}&id={sensorID}
```json
{
	"davis-013d4d": {
		"weather_station": {
			"id": "davis-013d4d",
			"timestamp": "2021-03-08T11:06:59.484000+0000",
			"avgwindspeed": 0.89,
			"bartrend": "Steady",
			"date": "19/08/2018 21:57:28",
			"dayet": 0.23,
			"dayrain": 0.0,
			"forecasticon": "Mostly Cloudy, Snow within 12 hours",
			"leafwetnesses": [-1.0, -1.0, -1.0, 0.0],
			"outsidehumidity": 54,
			"pm1": 14,
			"pm10": 14,
			"pm25": 14,
			"pressure": 964.71,
			"rainrate": 0.0,
			"soilmoistures": [-1.0, -1.0, -1.0, -1.0],
			"solarradiation": 46,
			"temperature": 3.94,
			"uv": 255,
			"winddirection": 316,
			"windspeed": 0.0
		}
	}
}
```

# Rules List GET /rules
```json
[
	{
		"id": "test",
		"name": "ExampleRule"
	}
]
```

# Rule GET /rule/{ruleID}
```json
{
  "id": "test",
  "name": "ExampleRule",
  "description": "Example rule for testing purposes.",
  "sensors": ["elsysco2-048e67"],
  "geofences": {
    "geofence1": [48.395829, 9.994795, 10]
  },
  "condition": {
    "and": [
      {
        "<=": [
          {
            "sensor": ["co2", "elsysco2-048e67", "co2"]
          },
          500
        ]
      },
      {"geofence":  "geofence1"}
    ]
  },
  "actions": [
    {
      "action": "notification",
      "data": {}
    }
  ]
}
```
