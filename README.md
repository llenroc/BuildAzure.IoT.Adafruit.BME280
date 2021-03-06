# BuildAzure.IoT.Adafruit.BME280
An [Adafruit BME280 (Pressure, Temp &amp; Humidity) Sensor](https://learn.adafruit.com/adafruit-bme280-humidity-barometric-pressure-temperature-sensor-breakout) library for Windows IoT Core

### Nuget Package
[![BuildAzure.IoT.Adafruit.BME280 Nuget Package](NugetCommand.png)](https://www.nuget.org/packages/BuildAzure.IoT.Adafruit.BME280)

### C# Usage

```csharp
var bme280Sensor = new BME280Sensor();

// Initialize BME280 Sensor
await bme280Sensor.Initialize();

// Read Temperature
var temp = bme280Sensor.ReadTemperature();

// Read Humidity
var humidity = bme280Sensor.ReadHumidity();

// Read Barometric Pressure
var pressure = bme280Sensor.ReadPressure();

// Read Altitude
const float seaLevelBarometricPressure = 1022.00f;
var altitude = bmd280Sensor.ReadAltitude(seaLevelBarometricPressure);
```

### Wiring Diagram
Here's a simple Fritzing diagram that shows the expected wiring of the [Adafruit BME280 sensor](https://learn.adafruit.com/adafruit-bme280-humidity-barometric-pressure-temperature-sensor-breakout) with a Raspberry Pi 2 or 3:

![BMD280 Raspberry Pi Wiring Diagram](BME280Fritzing.png)

### Examples
The [Weather Station V 3.0 project on Hackster.io](https://www.hackster.io/23021/weather-station-v-3-0-b8b8bc) provides a simple tutorial on using this library in a new UWP app. Also, the full source code for that project is available at the following location:

[https://github.com/BuildAzure/AdafruitBME280WeatherStation](https://github.com/BuildAzure/AdafruitBME280WeatherStation)

### Origins
This code was originally posted as part of the [Weather Station V 2.0 project](https://www.hackster.io/windows-iot/weather-station-v-2-0-8abe16) on [hackster.io](http://hackster.io). Since that project wasn't released using any reusable Nuget libraries for working with the Adafruit BME280 sensor, this project was created to borrow the BME280 code and release that out as a Nuget package for others to consume. Thankfully it's all licensed under the MIT License, and so is this project!
