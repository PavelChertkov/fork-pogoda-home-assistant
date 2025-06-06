![version_badge](https://img.shields.io/badge/minimum%20HA%20version-2025.4-red)

# Yandex weather data provider for Home Assistant

This custom integration is providing weather component and set of sensors based on data from [yandex pogoda](https://yandex.ru/pogoda/b2b/smarthome) service.

## Important

Currently Yandex provides free keys for Home Assistant for new users here: https://yandex.ru/pogoda/b2b/smarthome

## Installation

### HACS

1. Install Home Assistant Community Store(HACS) on your Home Assistant
2. Start typing "Pogoda" in HACS search field
3. Select: Yandex Pogoda
4. Press "Download" button
5. Restart Home Assistant

## Configuration

1. Go to Yandex [smarthome page](https://yandex.ru/pogoda/b2b/smarthome)
2. Get free Yandex.Weather.API key
3. It may require up to 5 minutes for Yandex to activate new key.
4. Save API key
5. Go to Home Assistant settings
   - Integrations
   - Add
   - Start typing "Yandex Pogoda" _(clean browser cache if nothing found)_
   - Add integration
   - Put API key into API key field

## Usage

### Weather

- attribute forecast icons with Yandex forecast weather state images
- temperature, wind speed and other unit may be customized
- forecast data is available for periods (night/morning/day/evening)

#### attributes

- native Yandex.Weather pictures for weather condition

### Sensors

- `Condition HomeAssistant` -- Current HomeAssistant weather [condition](https://www.home-assistant.io/integrations/weather/#condition-mapping).
- `Condition Yandex` -- Current Yandex.Weather.API [condition](https://yandex.ru/dev/weather/doc/ru/concepts/spectaql#values2).
- `Data update time` -- when weather data was updated.
- `Feels like temperature` -- shows how comfortable the weather conditions are, taking into account humidity, wind strength and other weather factors.
- `Minimal forecast temperature` -- minimal temperature for all forecast periods.
- `Temperature` -- The temperature value in the shade at a height of 2 meters from the ground surface.
- `Wind bearing` -- The angle of the wind direction.
- `Wind gust` -- The speed of wind gusts.
- `Wind speed` -- Wind speed at a height of 10 meters from the ground surface.

Some sensors are disabled by default.

### Events

- integration will fire events on weather condition changes. This events may be used for triggering automatizations.
