# Weather Application

The Weather Application is a user-friendly platform designed to provide accurate and real-time weather forecasts, earthquake alerts, and air quality updates. With a sleek and responsive interface, users can easily access hourly, daily, and 5-day weather forecasts for any city worldwide. The application also features a dark mode, customizable units for temperature and wind speed, and a rotating weather fact section to keep users informed and engaged.

Additionally, the app integrates earthquake and tsunami alerts, local time updates, and curated weather-related news articles. By combining essential weather data with a visually appealing design, the Weather Application aims to be your go-to dashboard for staying informed about the environment around you.

# UX

The Weather Application is designed for individuals who want to stay informed about weather conditions, environmental alerts, and related news in a convenient and visually appealing way. The target audience includes travelers, outdoor enthusiasts, and anyone who needs accurate and timely weather updates to plan their day or stay safe during extreme conditions.

## User Stories

- As a traveler, I want to check the weather forecast for my destination, so that I can pack appropriately.
- As an outdoor enthusiast, I want to know the air quality index, so that I can decide if it’s safe to exercise outside.
- As a concerned citizen, I want to receive earthquake and tsunami alerts, so that I can take necessary precautions.
- As a casual user, I want to read interesting weather facts, so that I can learn something new while using the app.
- As a user, I want to switch between light and dark modes, so that I can use the app comfortably in different lighting conditions.
- As a news reader, I want to see curated weather-related news articles, so that I can stay updated on global weather events.

## Design Process

To ensure a seamless user experience, wireframes and mockups were created during the design phase. These visual guides helped in planning the layout, navigation, and overall functionality of the application. You can view the wireframes and mockups in the `design` directory of this project or access them [here](#). The design process focused on simplicity, responsiveness, and accessibility to cater to a wide range of users.

# Features

## Existing Features

- **Real-Time Weather Forecasts**: Allows users to view hourly, daily, and 5-day weather forecasts for any city worldwide by entering the city name in the search bar. This feature is implemented in the `forecast` functions.
- **Earthquake and Tsunami Alerts**: Provides users with real-time alerts about recent earthquakes and potential tsunamis, helping them stay prepared for emergencies.
- **Air Quality Index (AQI)**: Displays the air quality index for the selected city, enabling users to make informed decisions about outdoor activities.
- **Dark Mode**: Offers a toggle to switch between light and dark themes, improving usability in different lighting conditions. This feature is implemented using localStorage to save user preferences.
- **Rotating Weather Facts**: Displays interesting weather facts that rotate periodically, keeping users engaged and informed.
- **Curated Weather News**: Fetches and displays the latest weather-related news articles using the NewsAPI, allowing users to stay updated on global weather events.
- **Local Time Updates**: Shows the local time for the selected city, helping users plan their activities effectively.
- **Recent Searches**: Saves and displays a list of recent city searches, allowing users to quickly revisit previous queries.

## Features Left to Implement

- **Severe Weather Notifications**: Add push notifications to alert users about severe weather conditions in real-time.
- **Interactive Weather Maps**: Integrate interactive maps to display weather patterns, radar, and satellite imagery.
- **Multi-Language Support**: Provide translations for the application to cater to a global audience.
- **User Accounts**: Allow users to create accounts to save preferences, favorite locations, and receive personalized alerts.

# Technologies Used

- **HTML5**: [HTML5](https://developer.mozilla.org/en-US/docs/Web/HTML) was used to structure the content of the application and ensure semantic, accessible markup.
- **CSS3**: [CSS3](https://developer.mozilla.org/en-US/docs/Web/CSS) was used to style the application, including implementing responsive design and dark mode.
- **JavaScript**: [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) was used to add interactivity, fetch data from APIs, and handle dynamic content updates.
- **JQuery**: [JQuery](https://jquery.com/) was used to simplify DOM manipulation and event handling, making the code more concise and easier to maintain.
- **NewsAPI**: [NewsAPI](https://newsapi.org/) was used to fetch curated weather-related news articles to keep users informed about global weather events.
- **OpenWeatherMap API**: [OpenWeatherMap](https://openweathermap.org/api) was used to retrieve real-time weather data, including forecasts, air quality, and severe weather alerts.
- **LocalStorage**: [LocalStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) was used to save user preferences, such as theme settings and recent searches, for a personalized experience.
- **Git**: [Git](https://git-scm.com/) was used for version control to track changes and collaborate effectively during development.
- **Visual Studio Code**: [VS Code](https://code.visualstudio.com/) was the primary code editor used for writing and debugging the application.

# Testing

To ensure the Weather Application works as intended, all user stories from the UX section were tested manually and automated where feasible. Below is a summary of the testing process, including scenarios, results, and any issues encountered.

## User Story Testing

### 1. Real-Time Weather Forecasts
- **Scenario**: Enter a city name in the search bar and view the hourly, daily, and 5-day weather forecasts.
  - **Steps**:
    1. Enter "New York" in the search bar.
    2. Verify that the weather data for New York is displayed, including temperature, wind speed, and weather conditions.
  - **Result**: Weather data is displayed correctly for the entered city.

### 2. Earthquake and Tsunami Alerts
- **Scenario**: Receive alerts for recent earthquakes and potential tsunamis.
  - **Steps**:
    1. Simulate an earthquake alert using mock API data.
    2. Verify that the alert is displayed prominently on the dashboard.
  - **Result**: Alerts are displayed correctly.

### 3. Air Quality Index (AQI)
- **Scenario**: View the air quality index for a selected city.
  - **Steps**:
    1. Search for "Los Angeles."
    2. Verify that the AQI is displayed with appropriate labels (e.g., "Good," "Moderate").
  - **Result**: AQI is displayed accurately.

### 4. Dark Mode
- **Scenario**: Toggle between light and dark themes.
  - **Steps**:
    1. Click the dark mode toggle.
    2. Verify that the theme changes and the preference is saved in localStorage.
  - **Result**: Dark mode works as expected and persists across sessions.

### 5. Curated Weather News
- **Scenario**: Display weather-related news articles.
  - **Steps**:
    1. Verify that the news section fetches and displays articles using the NewsAPI.
    2. Check that each article includes a title, source, and image (if available).
  - **Result**: News articles are displayed correctly.

### 6. Local Time Updates
- **Scenario**: Show the local time for the selected city.
  - **Steps**:
    1. Search for "Tokyo."
    2. Verify that the local time for Tokyo is displayed.
  - **Result**: Local time updates correctly.

### 7. Recent Searches
- **Scenario**: Save and display a list of recent city searches.
  - **Steps**:
    1. Search for multiple cities (e.g., "Paris," "London").
    2. Verify that the recent searches list updates and displays the cities.
  - **Result**: Recent searches are saved and displayed correctly.

## Browser and Screen Size Testing
- **Browsers Tested**: Chrome, Firefox, Edge.
- **Screen Sizes Tested**: Desktop (1920x1080), Tablet (768x1024), Mobile (375x667).
- **Results**: The application is fully responsive and works well across all tested browsers and screen sizes.

## Bugs and Issues
- **Issue**: Occasionally, the NewsAPI returns an error due to rate limits.
  - **Resolution**: Added error handling to display a user-friendly message when the API fails.
- **Issue**: On smaller screens, some elements overlap in the weather forecast section.
  - **Resolution**: Adjusted CSS to improve layout responsiveness.

## Automated Testing
- Automated tests were written for key features using [Jest](https://jestjs.io/) and [Puppeteer](https://pptr.dev/).
- **Test Files**: Located in the `tests` directory.
- **How to Run**:
  1. Install dependencies: `npm install`.
  2. Run tests: `npm test`.

For detailed test results, refer to the `tests` directory or the [Testing Documentation](./tests/README.md).


