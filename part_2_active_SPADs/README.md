# Part 2: Active Single Photon Imaging

Hands-on demo using the AMS TMF8820 time-of-flight sensor to explore active SPAD time-of-flight imaging.

**What you'll learn:**
- Capture and interpret transient histograms from a real ToF sensor
- Understand the hardware layout of a SPAD-based LiDAR system
- Implement your own distance estimation algorithm

## Hardware Setup

Assemble the setup as shown below using the provided parts. The USB and I2C cables are reversible.

- **AMS TMF8820 Sensor** — [SparkFun Qwiic Mini ToF Imager](https://www.sparkfun.com/sparkfun-qwiic-mini-dtof-imager-tmf8820.html)
- **Microcontroller** — [SparkFun Qwiic Pro Micro](https://www.sparkfun.com/sparkfun-qwiic-pro-micro-usb-c-atmega32u4.html)
- **Cable** — [SparkFun Qwiic Cable](https://www.sparkfun.com/qwiic-cable-100mm.html)
- **USB** — USB C to C cable

![Hardware setup](media/hardware_setup.png)

## Software Setup

The microcontroller comes pre-flashed with [custom firmware](https://github.com/uwgraphics/ProximityPlanarRecovery/tree/main/arduino) that forwards TMF8820 measurements to your computer. Just plug it in.

### Verify

Make sure you've set up the environment at the repository root first (see [README](../README.md#setup)), then:

```bash
cd part_2_active_SPADs
python live_vis.py
```

If the port isn't auto-detected, pass it explicitly with `--port` (e.g., `/dev/ttyACM0` on Linux, `COM1` on Windows, `/dev/tty.usbserial-XXXXXX` on macOS).

## Activities

1. **[Recreate Transient Histograms](activity1.md)** — Use the TMF8820 to produce histograms with specific shapes: one peak, three peaks, a slope, and more.

2. **[Identify Laser vs. Sensor](activity2.md)** — Figure out which cavity on the sensor board is the laser and which is the SPAD detector.

3. **[Estimate Distance](activity3.md)** — Write your own algorithm to estimate distance from a transient histogram and compare against the sensor's onboard estimate.
