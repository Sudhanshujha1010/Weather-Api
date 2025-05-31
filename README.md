**Weather App 🌤️** --

A beautiful, responsive weather application that provides real-time weather information for any city worldwide. Built with vanilla JavaScript and powered by the OpenWeatherMap API.

![Weather App](https://img.shields.io/badge/Status-Active-brightgreen)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![API](https://img.shields.io/badge/API-OpenWeatherMap-blue)

**✨ Features**

- **🌍 Global Weather Data**: Get weather information for any city worldwide
- **🎨 Beautiful UI**: Modern gradient design with smooth animations
- **📱 Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **🖼️ Dynamic Icons**: Weather-appropriate icons that change based on conditions
- **⚡ Real-time Data**: Live weather updates from OpenWeatherMap API
- **❌ Error Handling**: User-friendly error messages for invalid city names
- **🌡️ Detailed Information**: Temperature, humidity, and wind speed display

**🖥️ Demo**

Enter any city name to get instant weather information including:
- Current temperature in Celsius
- Weather conditions with appropriate icons
- Humidity percentage
- Wind speed in km/h

**🚀 Quick Start**

### Prerequisites
- A modern web browser
- Internet connection for API calls
- OpenWeatherMap API key (free registration required)

**Installation**

1. **Clone the repository**:
```bash
git clone https://github.com/yourusername/weather-app.git
```

2. **Navigate to the project directory**:
```bash
cd weather-app
```

3. **Get your API key**:
   - Visit [OpenWeatherMap](https://openweathermap.org/api)
   - Sign up for a free account
   - Generate your API key

4. **Configure the API key**:
   - Open `app.js`
   - Replace the existing API key with your own:
   ```javascript
   const apiKey = "YOUR_API_KEY_HERE";
   ```

5. **Launch the application**:
```bash
# Open index.html in your browser
# Or use a local server (recommended)
python -m http.server 8000
# Then visit http://localhost:8000
```

**📁 Project Structure**

```
weather-app/
│
├── index.html          # Main HTML structure
├── style.css           # Responsive CSS styling
├── app.js              # JavaScript functionality
├── assets/             # Image assets directory
│   ├── search.png      # Search button icon
│   ├── clouds.png      # Cloudy weather icon
│   ├── clear.png       # Clear weather icon
│   ├── rain.png        # Rainy weather icon
│   ├── drizzle.png     # Drizzle weather icon
│   ├── mist.png        # Misty weather icon
│   ├── humidity.png    # Humidity indicator icon
│   └── wind.png        # Wind speed indicator icon
└── README.md           # Project documentation
```

**🎯 How to Use**

1. **Enter City Name**: Type the name of any city in the search input field
2. **Search**: Click the search button or press Enter
3. **View Results**: See the current weather information displayed with:
   - Temperature in Celsius
   - Weather condition icon
   - City name
   - Humidity percentage
   - Wind speed in km/h
4. **Try Different Cities**: Search for multiple cities to compare weather conditions

**🛠️ Technical Details**

### Technologies Used
- **HTML5**: Semantic structure and accessibility
- **CSS3**: Modern styling with gradients and flexbox
- **Vanilla JavaScript**: API integration and DOM manipulation
- **OpenWeatherMap API**: Real-time weather data

### API Integration
- **Endpoint**: `https://api.openweathermap.org/data/2.5/weather`
- **Method**: GET requests with city name and API key
- **Response Format**: JSON with weather data
- **Units**: Metric system (Celsius, km/h)

**Key Features Implementation**

#### Weather Data Fetching
```javascript
async function checkWeather(city) {
    const response = await fetch(apiUrl + city + `&appid=${apiKey}`);
    // Handle response and update UI
}
```

#### Dynamic Icon System
Weather icons change automatically based on API response:
- ☁️ Clouds
- ☀️ Clear
- 🌧️ Rain
- 🌦️ Drizzle
- 🌫️ Mist

#### Error Handling
- Invalid city names show user-friendly error messages
- Network errors are handled gracefully
- 404 responses trigger error display

**🎨 Customization**

### Changing the Color Scheme
Edit the gradient in `style.css`:
```css
.card {
    background: linear-gradient(135deg, #00feba, #5b548a);
    /* Change colors to your preference */
}
```

### Adding New Weather Conditions
Extend the weather icon logic in `app.js`:
```javascript
if(data.weather[0].main == "Snow"){
    weatherIcon.src = "assets/snow.png";
}
```

### Modifying Temperature Units
Change units in the API URL:
```javascript
// For Fahrenheit
const apiUrl = "https://api.openweathermap.org/data/2.5/weather?&units=imperial&q=";

// For Kelvin (default)
const apiUrl = "https://api.openweathermap.org/data/2.5/weather?&q=";
```

**🔧 Configuration**

### API Settings
```javascript
const apiKey = "your-api-key-here";
const apiUrl = "https://api.openweathermap.org/data/2.5/weather?&units=metric&q=";
```

### Styling Variables
Key CSS properties you can customize:
- Card width: `max-width: 470px`
- Border radius: `border-radius: 20px`
- Font family: `font-family: 'Poppins', 'sans-serif'`
- Background gradient: `linear-gradient(135deg, #00feba, #5b548a)`

**🐛 Troubleshooting**

**Common Issues**

**API key not working:**
- Verify your API key is correct and active
- Check if you've exceeded the free tier limits
- Ensure the API key is properly configured in `app.js`

**Cities not found:**
- Check spelling of city names
- Try using different city name formats
- Some small cities might not be in the database

**Images not loading:**
- Verify all image files are in the `assets/` directory
- Check file names match exactly (case-sensitive)
- Ensure proper file extensions (.png)

**Styling issues:**
- Clear browser cache
- Check if `style.css` is loading properly
- Verify CSS file path is correct

**📱 Browser Support**

- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ✅ Opera 47+

**🤝 Contributing**

Contributions are welcome! Here's how to contribute:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit changes**: `git commit -m 'Add amazing feature'`
4. **Push to branch**: `git push origin feature/amazing-feature`
5. **Open a Pull Request**
