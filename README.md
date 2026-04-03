# 🌤️ Weather App

A clean and responsive **Weather App** built with pure **HTML, CSS, and JavaScript** that shows real-time weather data for any city in the world using the OpenWeatherMap API.

---

## 🚀 Live Demo

> Search any city and get instant weather info — temperature, humidity, wind speed, and a matching weather icon!

---

## ✨ Features

- 🔍 Search weather by city name
- 🌡️ Shows real-time temperature in °C
- 💧 Displays humidity percentage
- 💨 Shows wind speed in km/h
- 🌦️ Dynamic weather icons (Clouds, Clear, Rain, Drizzle, Mist)
- ❌ Error handling for invalid city names
- 📱 Fully responsive — works on mobile and desktop

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| HTML5 | Page structure |
| CSS3 | Styling & gradient design |
| JavaScript (ES6+) | Logic & API calls |
| OpenWeatherMap API | Live weather data |

---

## 📁 Project Structure

```
Weather-app/
│
├── index.html        # Main HTML file
├── style.css         # All CSS styles
└── images/
    ├── search.png    # Search button icon
    ├── clouds.png    # Cloudy weather icon
    ├── clear.png     # Clear/sunny icon
    ├── rain.png      # Rain icon
    ├── drizzle.png   # Drizzle icon
    ├── mist.png      # Mist icon
    ├── humidity.png  # Humidity icon
    └── wind.png      # Wind icon
```

---

## ⚙️ Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/saad-aids/Weather-app.git
cd Weather-app
```

### 2. Get your free API key

- Go to [https://openweathermap.org](https://openweathermap.org)
- Create a free account
- Go to **API Keys** section and copy your key

### 3. Add your API key

Open `index.html` and replace the API key on this line:

```javascript
const apiKey = "YOUR_API_KEY_HERE";
```

### 4. Run the app

Simply open `index.html` in your browser — no server needed!

```bash
# Or use VS Code Live Server extension for best experience
```

---

## 🔌 API Used

This app uses the **OpenWeatherMap Current Weather API**:

```
https://api.openweathermap.org/data/2.5/weather?units=metric&q={city}&appid={apiKey}
```

| Parameter | Description |
|---|---|
| `q` | City name entered by user |
| `units=metric` | Temperature in Celsius |
| `appid` | Your API key |

---

## 📸 Screenshots

> *(Add your app screenshots here)*

| Search | Result | Error |
|---|---|---|
| ![Search](#) | ![Result](#) | ![Error](#) |

---

## 🧠 How It Works

1. User types a city name and clicks the search button
2. JavaScript calls the OpenWeatherMap API using `fetch()`
3. If the city is valid — weather data is displayed
4. If the city is invalid — an error message is shown
5. The weather icon changes dynamically based on weather type

```javascript
async function checkWeather(city) {
  const response = await fetch(apiUrl + city + '&appid=' + apiKey);
  if (!response.ok) { /* show error */ return; }
  const data = await response.json();
  // update DOM with data.name, data.main.temp, etc.
}
```

---

## 🌈 Weather Icons Supported

| Weather | Icon Used |
|---|---|
| ☁️ Clouds | clouds.png |
| ☀️ Clear | clear.png |
| 🌧️ Rain | rain.png |
| 🌦️ Drizzle | drizzle.png |
| 🌫️ Mist | mist.png |

---

## 🚀 Future Improvements

- [ ] Add Enter key support for search
- [ ] Show 5-day weather forecast
- [ ] Add loading spinner while fetching
- [ ] Detect user's current location automatically
- [ ] Add dark/light mode toggle

---

## 👨‍💻 Author

**Saad**
- GitHub: [@saad-aids](https://github.com/saad-aids)
- YouTube: https://youtube.com/@saadsadikshaikh?si=ARJvvM-cQNfXlUeh

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## ⭐ Show Your Support

If you found this project helpful, please give it a **⭐ star** on GitHub!

It means a lot and helps others find this project too. 🙏

