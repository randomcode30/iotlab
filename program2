#include "DHT.h"   // Include DHT sensor library

#define DHTPIN 2          // Data pin connected to digital pin 2
#define DHTTYPE DHT11     // Sensor type (Change to DHT22 if needed)

DHT dht(DHTPIN, DHTTYPE);  // Create DHT object

void setup() {
  Serial.begin(9600);   // Start serial communication
  Serial.println("DHT Sensor Reading Example");
  dht.begin();          // Initialize sensor
}

void loop() {
  float humidity = dht.readHumidity();       // Read humidity
  float temperature = dht.readTemperature(); // Read temperature in Celsius

  if (isnan(humidity) || isnan(temperature)) {
    Serial.println("Failed to read from DHT sensor!");
    delay(2000);
    return;
  }

  Serial.print("Temperature: ");
  Serial.print(temperature);
  Serial.print(" °C | Humidity: ");
  Serial.print(humidity);
  Serial.println(" %");

  delay(5000); // Wait 5 seconds
}
