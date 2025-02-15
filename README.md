Weather Forecast Notifier (C++ & cURL)

Overview
This C++ program fetches real-time weather data from the Weatherstack API and determines if bad weather conditions, such as heavy cloud cover, are approaching the specified location. If cloud coverage exceeds 50 percent, the program notifies the user that rain is expected within 30 minutes.

Features

   - Fetches real-time weather data using cURL.
   - Parses JSON responses with nlohmann/json.
   - Checks for high cloud cover levels.
   - Displays alerts if bad weather is approaching.

How It Works

  - The program constructs an API request URL with the user’s location.
  - It uses cURL to send an HTTP request to the Weatherstack API.
  - The response is stored in a string and parsed as JSON.
  -  The program checks if cloud cover exceeds 50 percent.
  - If cloud cover is too high, the user is notified of incoming rain.
    Otherwise, it informs the user that the weather is clear.

Code Breakdown

Handling HTTP Responses
This function processes the HTTP response from the API and appends it to a string.

Setting Up the API Request
The API endpoint is constructed using a location, such as Bucharest, Romania, and the user’s API key.

Sending an HTTP Request

   - Initializes cURL.
   - Sends an HTTP request.
   - Stores the response in a string.

Parsing the JSON Response
Converts the API response from a string into a JSON object.

Checking for Bad Weather

   - If cloud cover is greater than 50 percent, it flags bad weather.
   - Retrieves weather descriptions and observation time.

Outputting the Weather Forecast

   - If bad weather is detected, it warns the user.
   - Otherwise, it informs the user that the weather is clear.

Requirements

   - C++ compiler (GCC, Clang, or MSVC)
   - libcurl installed
   - Weatherstack API key

How to Run

   - Replace "YOUR_ACCESS_KEY" with your actual API key in the code.
   - Compile the program using the following command:
   - g++ -o weather_notifier weather.cpp -lcurl
   - Run the executable:
    ./weather_notifier
