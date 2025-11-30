1. 重要提示

此系统目前处于早期测试阶段。
MQ传感器部分功能未测试，为此系统提供了随机模拟数据生成。

2. 系统设计说明

此系统基于ESP32、蜂鸣器、OLED(SSD1306)、MQ2传感器、Blynk IoT平台及外围硬件组件构建。

使用前请配置以下常量：
`BLYNK_TEMPLATE_ID`
`BLYNK_TEMPLATE_NAME`
`BLYNK_AUTH_TOKEN`
`WiFi credentials`
`namespace HardwareConfig`

3. 使用说明与注意事项

`SensorConfig`命名空间提供传感器配置的可调参数。`RL`为负载电阻，请按需调整相关参数。
注意：用户须自行校准传感器，并将校准后的传感器内部电阻值填入`SensorConfig`中的`RO`变量。
为限制MQ传感器最高输出电压以保护ESP32，`SensorConfig`中定义了分压电路，请相应调整参数。

`TimingConfig`和`DisplayConfig`命名空间提供额外的配置选项。
注意：可能受性能限制或代码效率，系统的动画效果可能无法达到理想情况。

请在Blynk回调函数中修改传感器数据来源。
