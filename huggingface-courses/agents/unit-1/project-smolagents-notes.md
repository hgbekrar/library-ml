link for the project :

> [Tempered](https://huggingface.co/spaces/hgbekrar/Tempered)

Ask agent Tempered for the temperature anywhere in the world !
working chatbot Agent, 
tools : 
- get_current_temperature(latitude:float, longitude:float)-> str
- get_coordinates(city_name: str) -> tuple[float,float]
- get_current_time_in_timezone(timezone: str) -> str

he works thanks to https://open-meteo.com/ free API !


you can guess their description (a shame to say this after completing unit 1!) if you are interested in how they work look at the app.py file in the repo above.


this repo contains many (hundreds or even thousands) [free APIs](https://github.com/public-apis/public-apis)
