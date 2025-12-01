# Weather Dashboard

WeatherDashboard is a lightweight **React-based weather application** that displays real-time weather information for any city.  
The project was built to practice frontend architecture, API integration, and UI state management.

The application consumes an external weather API and presents clean, structured weather data to the user.

---

## Project Structure

- /src  
    - App.js  
    - components/  
        - SearchBox.jsx  
        - WeatherCard.jsx  
    - services/  
        - weatherService.js  
    - styles/  

- /public  
    - index.html  
    - icons / assets (if any)

---

## Key Concepts

### Weather Search
Users can:

- Search for a city  
- Fetch current weather (temperature, humidity, conditions, wind speed, etc.)  
- Display a simple and responsive weather card  

### API Integration
The app communicates with a third-party weather provider (e.g. OpenWeatherMap).  
All API configurations are handled through environment variables:
```bash
REACT_APP_WEATHER_API_KEY=<your_api_key>
```

`.env` is excluded from version control.

### Component-based Architecture
The UI is composed of small reusable components that handle:

- Input  
- Weather display  
- API state (loading/error)  

### State Management
State is handled using React built-in hooks (`useState`, `useEffect`)  
and async API calls with `fetch` or `axios`.

---

## Running the Project

Install dependencies:

```bash
npm install
```

or:

```bash
yarn install
```

Start development server:
```bash
npm start
```

The app will run on:
```bash
http://localhost:3000
```
---

## Example Usage
```bash
import { getWeather } from "./services/weatherService";

getWeather("Oslo").then(data => {
  console.log(data.temperature);
});
```

---

## Requirements
- Node.js (LTS recommended)
- React
- External weather API key

---

## Future Improvements
- 5-day forecast
- Temperature unit toggle (°C/°F)
- Error states (invalid city, network issues)
- Responsive layout improvements
- Deployment on Netlify / Vercel / GitHub Pages