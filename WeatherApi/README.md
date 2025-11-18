# Weather API

A simple ASP.NET Core Web API that provides weather forecast data.

## Features

- RESTful API endpoint for retrieving weather forecasts
- Swagger/OpenAPI documentation
- Returns 5-day weather forecast with temperature and weather summary
- Built with .NET 8.0

## Prerequisites

- [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) or later

## Getting Started

### Build the Project

```bash
dotnet build
```

### Run the API

```bash
dotnet run
```

The API will start and listen on:
- HTTP: `http://localhost:5279`
- HTTPS: `https://localhost:7214`

### Access Swagger UI

Open your browser and navigate to:
```
http://localhost:5279/swagger
```

The Swagger UI provides interactive API documentation where you can test the endpoints.

## API Endpoints

### GET /WeatherForecast

Returns a 5-day weather forecast.

**Response Example:**
```json
[
  {
    "date": "2025-11-19",
    "temperatureC": 25,
    "temperatureF": 76,
    "summary": "Warm"
  },
  {
    "date": "2025-11-20",
    "temperatureC": 18,
    "temperatureF": 64,
    "summary": "Cool"
  }
]
```

**Response Fields:**
- `date`: The forecast date (ISO 8601 format)
- `temperatureC`: Temperature in Celsius
- `temperatureF`: Temperature in Fahrenheit
- `summary`: Weather condition summary

## Testing with cURL

```bash
curl http://localhost:5279/WeatherForecast
```

## Testing with HTTP file

The project includes a `WeatherApi.http` file that can be used with Visual Studio Code's REST Client extension or Visual Studio's built-in HTTP client.

## Project Structure

```
WeatherApi/
├── Controllers/
│   └── WeatherForecastController.cs  # API controller
├── Properties/
│   └── launchSettings.json            # Launch configuration
├── appsettings.json                   # Application settings
├── appsettings.Development.json       # Development settings
├── Program.cs                         # Application entry point
├── WeatherForecast.cs                 # Data model
└── WeatherApi.csproj                  # Project file
```

## Technologies Used

- ASP.NET Core 8.0
- Swagger/OpenAPI (Swashbuckle)
- Minimal APIs with Controllers

## Development

The API uses the standard ASP.NET Core configuration with:
- Dependency injection
- Logging
- Development environment configuration
- HTTPS redirection
- Controller-based routing

## License

This project is part of the test-fork repository.
