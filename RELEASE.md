EPICS IOC for Nordic thingy:52

Currently supported sensors:

- Step counter
- Air quality (gas)
- Gravity vectors
- Quaternions
- Tap
- Battery
- Accelerometer
- Gyroscope
- Compass
- Roll, pitch, yaw
- Heading
- Temperature
- Humidity
- Pressure
- Button
- LED (read only)

R1-0
=================

R1-0-4 4/19/19
----
- Add support for step counter, air quality (gas), gravity vectors
- Rotation matrix supported but too long to be stored in stringin record

R1-0-3 4/17/19
----

- Add support for quaternions, tap sensor
- Move MAC address declaration to thingyConfig() IOC command
- Add forward links to read/write PVs
- Add documentation to database files

R1-0-2 4/12/19
----

- Add support for battery (read), accelerometer, gyroscope, compass
- Stop notifications on keyboard interrupt
- Fix buffer sizes for UUIDs

R1-0-1 4/4/19
-----

- Add support for Euler roll/pitch/yaw and heading
- More descriptive errors
- Disconnect from device on keyboard interrupt

R1-0-0 3/29/19
-----

- Supports temperature, humidity, pressure, orientation, button UUIDs (notify) and LED UUID (read)
- Notify UUIDs split between numeric values and string values (notifyNumber.template and notifyString.template)
- Notify UUID records trigger their own processing upon receipt of notifcation from device, read UUIDs must be
  triggered manually with a periodic scan
- Parse device response according to specific UUID, using Nordic's specifications
	- https://nordicsemiconductor.github.io/Nordic-Thingy52-FW/documentation/firmware_architecture.html
