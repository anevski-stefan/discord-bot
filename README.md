# Discord Weather Forecast Bot

This is a Discord bot built with Node.js that provides weather & astronomical forecasts using the [WeatherAPI](https://www.weatherapi.com/).

## Prerequisites

- Node.js
- npm
- A Discord bot token
- A WeatherAPI key

## Project Structure

```
discord-bot/
├── src/
│   ├── commands/     # Bot commands
│   ├── events/       # Discord event handlers
│   ├── requests/     # API request handlers
│   └── index.js      # Main bot entry point
├── package.json
└── .env
```

## Dependencies

- discord.js (v14.15.3) - Discord bot framework
- axios (v1.7.2) - HTTP client for API requests
- dotenv (v16.4.5) - Environment variable management
- nodemon (v3.1.4) - Development dependency for auto-reloading

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/anevski-stefan/discord-bot.git
   cd discord-bot
   ```

2. Install the required dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add the following environment variables:

   ```env
   DISCORD_TOKEN=your-discord-token
   CLIENT_ID=your-client-id
   GUILD_ID=your-guild-id
   WEATHER_API_KEY=your-weather-api-key
   ```

   Replace `your-discord-token`, `your-client-id`, `your-guild-id`, and `your-weather-api-key` with your actual values.

## Running the Bot

1. Start the bot:

   ```bash
   npm run start
   ```

   For development with auto-reloading:

   ```bash
   npm run dev
   ```

2. Invite the bot to your server using the OAuth2 URL:

   ```text
   https://discord.com/oauth2/authorize?client_id=your-client-id&scope=bot&permissions=YOUR_PERMISSIONS
   ```

   Replace `your-client-id` with your actual client ID and `YOUR_PERMISSIONS` with the necessary permissions for your bot.

## Commands

- `/forecast [location] (optional argument units)`: Get the weather forecast for the specified location. Optionally, specify the units (e.g., metric or imperial).
- `/astro [location]`: Get astronomical data (sun rise/set, moon phase, etc.) for the specified location.
- `/ping`: Check the bot's response time and connectivity.

## Example

To get the weather forecast for New York, type the following command in your Discord server:

```text
/forecast New York
```

For astronomical data:
```text
/astro London
```
