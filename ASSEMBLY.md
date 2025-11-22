# Assembly Instructions

*Build it. Control it. Enjoy it.*

## 1. Mounting Components

1. Secure the **NodeMCU** on the side wall of the enclosure using M3 screws.
2. Secure the **4-channel relay board** on the bottom of the enclosure.
3. Ensure both boards are firmly fixed — usually two screws per board are sufficient.

---

## 2. Wiring NodeMCU to Relay Board

Use Dupont jumper wires:

- D0 → IN1
- D1 → IN2
- D2 → IN3
- D3 → IN4
- VCC → VCC
- GND → GND

---

## 3. LED Connection (optional)

- Connect LED to D5/D6 with a **150–300 Ω resistor** in series.
- Positive leg -- resistor -- D5/D6
- Negative leg -- GND
- Optional: connect LED for mode indication (D5 for AP, D6 for Wi-Fi).

---

## 4. Closing Enclosure

1. Place the lid onto the box.
2. Secure with M3 screws.
3. Connect power via **micro USB**.

---

## 5. AP Mode (Beginner / Offline Control)

No Wi-Fi or internet required — the kit works locally.

### Setup Instructions

1. Connect a 5V adapter to the micro USB port.
2. The LED will turn on, indicating power.
3. On your phone, tablet, or laptop, connect to Wi-Fi network `roVad_AP`.
4. Open a web browser and go to: `http://192.168.4.1`.
5. Control four relays via the interface.
6. Tap buttons to toggle appliances ON/OFF.

🎉 Congratulations! Your kit is operational in AP Mode.

⚠️ **Safety Note:** 
When connecting household appliances (110–250V AC), take proper precautions. Assembly and usage are at your own responsibility.

---

## 6. Wi-Fi Mode (Advanced / Remote Control)

Allows remote control via an MQTT server.

⚠️ **Note:** Supports **2.4GHz Wi-Fi networks only**.

### Setup Instructions

1. Complete steps 1–4 from the AP Mode setup.
2. On the web page `http://192.168.4.1`, click **MQTT Setup**.
3. Fill required fields:
   - Wi-Fi SSID and Password
   - MQTT Username and Password
   - Timezone (for relay timers)
   - Feed format:
     - Adafruit: `username/feeds/feedname`
     - Home Assistant: `any/feedname`
   - Select MQTT server.
4. Click **Submit**.
5. The second LED will blink while connecting to Wi-Fi.
6. Once connected, the LED remains steadily on. Now you can control the relays remotely via the app.

🎉 Congratulations! Your kit is now online and ready to receive remote commands.

⚠️ **Safety Note:** 
When connecting household appliances (110–250V AC), take proper precautions. Assembly and usage are at your own responsibility.

---

## 7. Relay Timer Configuration

- Each relay supports independent timers.
- Timers follow your configured timezone.
- Enable/disable timers in the app.
- Automatic ON/OFF scheduling allows appliances to operate without manual intervention.
- Sending proper command you can list all your set timers anytime

---
