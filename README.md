 * 1. Important Note
 * 
 * This system is currently in the early testing phase.
 * Some functions of the MQ sensor have not been tested.
 * Therefore, random simulated data generation is provided for this system.
 * 
 * 2. System Design Description
 * 
 * This system is built with ESP32, buzzer, OLED (SSD1306), MQ2 sensor, 
 * Blynk IoT platform, and peripheral hardware components.
 * 
 * Before use, please configure the following constants:
 * BLYNK_TEMPLATE_ID, BLYNK_TEMPLATE_NAME, BLYNK_AUTH_TOKEN
 * WiFi credentials
 * namespace HardwareConfig
 * 
 * 3. Usage Instructions and Notes
 * 
 * SensorConfig namespace provides adjustable parameters for sensor configuration.
 * RL represents the load resistor - adjust relevant parameters as needed.
 * Note: Users must calibrate the sensor and update the RO variable in SensorConfig 
 * with the calibrated sensor internal resistance. To protect ESP32 from damage by 
 * limiting MQ sensor's maximum output voltage, a voltage divider circuit is defined 
 * in SensorConfig namespace - adjust parameters accordingly.
 * 
 * TimingConfig and DisplayConfig namespaces provide additional configuration options.
 * Note: Due to potential performance limitations, some system animations may not 
 * achieve optimal speed.
 *    
 * Please modify the sensor data source in the Blynk callback function.
