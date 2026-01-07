## 🌤 Weather Information App

This Java-based desktop application provides **real-time weather information** for a given location using the **OpenWeatherMap API**. It features a friendly and interactive GUI created with **Java Swing**, allowing users to search for any city and view both the current conditions and an 8-day forecast. Additional features include unit conversion and search history tracking.


## 🌟 Features

* Retrieves current weather data for any entered city.
* Displays weather conditions, temperature, humidity, and wind speed.
* Shows an **8-day forecast** with clear formatting.
* Provides **dynamic weather icons** based on API response.
* Allows **switching** between **Celsius** and **Fahrenheit**.
* Tracks and displays **recent search history**.
* Responsive and clean user interface built with **Java Swing**.

## ⚙️ Prerequisites

* Java Development Kit (JDK) **8 or higher**.
* Internet connection to fetch real-time data.
* A valid API key from [OpenWeatherMap](https://openweathermap.org/api).
* `json-20240303.jar` library for parsing JSON.

## 💻 Installation

### Step 1: Clone the repository

```bash
git clone https://github.com/your-username/WeatherApp.git
cd WeatherApp
```

### Step 2: Replace API Key

Open the file `WeatherAPIService.java`, and **replace** the placeholder key with your actual OpenWeatherMap API key:

```java
private static final String API_KEY = "your_api_key_here";
```

### Step 3: Compile the code

```bash
javac -cp ".;lib/json-20240303.jar" WeatherApp.java WeatherAPIService.java
```

### Step 4: Run the app

```bash
java -cp ".;lib/json-20240303.jar" WeatherApp
```

## 🧱 Class Descriptions

### `WeatherApp.java`

Handles the full **graphical user interface** using Swing:

* `locationField`: for user input.
* `weatherInfoArea`: displays weather details.
* `iconLabel`: shows weather icon fetched via URL.
* `forecastLabel`: displays formatted forecast.
* `unitComboBox`: toggles temperature unit.
* `searchHistoryList`: stores past searches with timestamps.

### `WeatherAPIService.java`

Manages **API communication** and JSON parsing:

* `getWeather(String location)`: fetches current weather data.
* `getForecast(String location)`: fetches 5-day/3-hour forecast.
* Uses `HttpURLConnection` and `org.json` for requests and parsing.

## 💡 Example Usage

1. Enter a city name like `"Berlin"` in the input box.
2. Click `"Search"` to get weather info.
3. The app shows:

   * Weather icon (e.g., ☀️, ☁️)
   * Temperature, humidity, wind speed, condition description.
4. Forecast section updates with an 8-day preview.
5. Use the combo box to **switch units**.
6. Click any item in **search history** to reload data for that city.

## 📝 Notes
- Ensure internet connectivity for live API requests.
- API key management is essential for proper functionality.
- The app’s design is responsive and ready for both day-to-day use and future enhancements.

## 📚 References
Eck, D. J. (2022). *Introduction to Programming Using Java, Version 9*. Hobart and William Smith Colleges. https://math.hws.edu/javanotes/ 

JSON-java. (2021). *JSON in Java*. GitHub. https://github.com/stleary/JSON-java

OpenWeather. (n.d.). *Weather API – OpenWeatherMap*. Retrieved from https://openweathermap.org/api
