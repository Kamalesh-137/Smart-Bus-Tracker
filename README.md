# SmartBus Live Tracker

✅ **How to use:**
1. Open `index.html`.
2. Replace `YOUR_BLYNK_TOKEN` with your Blynk token.
3. Replace `YOUR_TOMTOM_API_KEY` with your TomTom Maps API key.
4. Upload the Arduino code to your ESP32 to push GPS lat/lon every few seconds.
5. Open `index.html` in your browser. It will show the live bus point and ETA to your stop.

✅ **Arduino Snippet:**
```cpp
float lat = gps.location.lat();
float lon = gps.location.lng();

Blynk.virtualWrite(V1, String(lat, 4));
Blynk.virtualWrite(V2, String(lon, 4));
```

Happy tracking! 🚍✨
