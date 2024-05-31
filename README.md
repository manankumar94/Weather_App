**Weather App**

This is a simple weather application that fetches and displays the current weather information for a given city using the OpenWeatherMap API.

**Features**

Displays the current temperature, humidity, and wind speed for a specified city.
Uses the OpenWeatherMap API to fetch weather data.
Simple and responsive user interface.
**Technologies Used:**
HTML
CSS
JavaScript
OpenWeatherMap API
Getting Started
Follow these instructions to get a copy of the project up and running on your local machine.

**Prerequisites**
You will need a modern web browser and an internet connection. Additionally, you need an API key from OpenWeatherMap. You can obtain one by creating a free account on OpenWeatherMap.

**Installation**
**Clone the repository to your local machine:**
git clone https://github.com/your-username/weather-app.git

**Navigate to the project directory:**
cd weather-app
Open index.html in your preferred web browser.

Usage
Open the application in your web browser.
Enter the name of the city for which you want to check the weather in the search box.
Click the search button to fetch and display the weather information.
Code Overview
**HTML**
The HTML file contains the structure of the weather app including the search box and the elements to display the weather information.

**CSS**
The CSS file contains the styling for the weather app. The card element is styled with a gradient background and other styles to make it visually appealing.

**JavaScript**
The JavaScript file contains the logic to fetch weather data from the OpenWeatherMap API and update the DOM with the fetched data.

**javascript**
const apiKey = "a962d249ba59d825e9704a9ef0c520cb";
const apiUrl = "https://api.openweathermap.org/data/2.5/weather?units=metric&q=";

const searchBox = document.querySelector(".search input");
const searchBtn = document.querySelector(".search button");

async function checkWeather(city) {
    const response = await fetch(apiUrl + city + `&appid=${apiKey}`);
    var data = await response.json();

    console.log(data);

    document.querySelector(".city").innerHTML = data.name;
    document.querySelector(".temp").innerHTML = Math.round(data.main.temp) + "°c";
    document.querySelector(".humidity").innerHTML = data.main.humidity + "%";
    document.querySelector(".wind").innerHTML = data.wind.speed + " km/h";
}
searchBtn.addEventListener("click", () => {
    checkWeather(searchBox.value);
});




**Contact**
For any inquiries or feedback, please contact mortal9193@gmail.com
