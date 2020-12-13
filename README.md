# Weather-API-Experiment

I'm currently working with `echo`, `curl`, and basic variable substitution to create a weather readout for Austin, Tx.

```
#!/bin/bash

# Working with Variables

API_key=testkey
city=Austin

curl -s "api.openweathermap.org/data/2.5/weather?q={$city}&appid={$API_key}&units=imperial"

echo "City:"; curl -s "api.openweathermap.org/data/2.5/weather?q={$city}&appid={$API_key}&units=imperial" | jq .name
echo "Temperature:"; curl -s "api.openweathermap.org/data/2.5/weather?q={$city}&appid={$API_key}&units=imperial" | jq .main.temp
echo "Feels Like:"; curl -s "api.openweathermap.org/data/2.5/weather?q={$city}&appid={$API_key}&units=imperial" | jq .main.feels_like
echo "Description:" ; curl -s "api.openweathermap.org/data/2.5/weather?q={$city}&appid={$API_key}&units=imperial" | jq .weather[].description
echo "Wind Speed:"; curl -s "api.openweathermap.org/data/2.5/weather?q={$city}&appid={$API_key}&units=imperial" | jq .wind.speed
```


I'll need to dedicate time to the git tutorials in order to remember how to commit this script from bash.
