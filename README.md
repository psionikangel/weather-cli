# Weather-CLI
A small tool to get the current weather, using the API provided by `openweathermap.org`

# Requirements
In order to use the tool, you need:
* `ruby v2.3.3+`
* An API key from `openweathermap.org`

# Usage
The script will work when called in two ways. You can supply either a latitude and longitude combo, or a `city_id` supported by `openweathermap.org`. The `city_id` is more precise, whereas the latitude and longitude can give you approximate results. In both case, it is mandatory to supply a working API key provided by `openweathermap.org`.

**If a `city_id` and a `latitude and longitude` pair are provided to the script, the `city_id` has priority.**

## Command line options
```
Usage: weather.rb [options]
    -k, --key APIKEY                 API key for the web service at api.openweathermap.org
    -c, --city CITYID                City_Id for the weather request
    -l, --latitude VAL               Latitude for the requested city
    -g, --longitude VAL              Longitude for the requested city
    -h, --help                       Displays Help
```

## Examples

### With a city_id (6077243 is Montreal)
```
ruby weather.rb -k 1377756ac67ca111111111fd0c44caa -c 6077243
```

Would output

```
Weather report for Montreal (45.51,-73.59)
Weather: Snow (light snow)
Temperature: -0.02 ℃
Humidity: 81%
Wind: 5.7 km/h

Data generated by api.openweathermap.org on 2017-11-23T22:28:00-05:00
```

### With a latitude and longitude (51.51 / -0.13 is London, UK)
```
ruby weather.rb -k 1377756ac67ca111111111fd0c44caa -l 51.51 -g -0.13
```

Would output

```
Weather report for London (51.51,-0.13)
Weather: Rain (light rain)
Temperature: 5.5 ℃
Humidity: 87%
Wind: 2.1 km/h

Data generated by api.openweathermap.org on 2017-11-23T22:20:00-05:00
```

## City IDs and Latitude/Longitude
You can get a complete list of city ids and their coordinates in json format with [this link](http://bulk.openweathermap.org/sample/city.list.json.gz).

_You can also try the following few provided below_

### Montreal
* ID: 6077243
* Lat: 45.508839
* Lon: -73.587807

### London, UK
* ID: 2643743
* Lat: 51.50853
* Lon: -0.12574

### Wellington, NZ
* ID: 2179538
* Lat: -41.283329
* Lon: 174.766663

### Moscow, RU
* ID: 524901
* Lat: 55.75222
* Lon: 37.615555

