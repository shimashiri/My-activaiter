# My-activaiter
Active in the hub gate
import requests

def get_weather(city):
    api_key = "https://wttr.in/"
    url = f"{api_key}{city}?format=3"
    try:
        response = requests.get(url)
        if response.status_code == 200:
            print(f"Weather in {city}: {response.text}")
        else:
            print("Error fetching weather data.")
    except Exception as e:
        print("Error:", e)

if __name__ == "__main__":
    city = input("Enter city name: ")
    get_weather(city)
