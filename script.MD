# 🎤 IoT Workshop — Full Day Instructor Script
### ESP32 · Wokwi · ThingSpeak · Hackathon
#### 9:30 AM – 4:30 PM

---

> **How to use this script**
> 
> 🎤 **SAY THIS** → exact words to speak out loud  
> 🎮 **GAME** → interactive activity with full instructions  
> 💡 **TIP** → behind-the-scenes instructor notes  
> 💻 **CODE** → paste this into Wokwi  
> ▶ **SLIDE N** → when to advance the presentation  

---

## 📋 Quick Agenda

| Time | Session | Slide |
|---|---|---|
| 9:30 – 10:00 | Kickoff + IoT Mindset | 1–5 |
| 10:00 – 11:00 | ESP32 Deep Dive — GPIO & PWM | 6–8 |
| 11:00 – 11:15 | ☕ Break | — |
| 11:15 – 12:45 | 🔥 Sensor Playground — 5 Sensors | 9–12 |
| 12:45 – 1:30 | 🍽️ Lunch | — |
| 1:30 – 2:30 | Networking + ThingSpeak Cloud | 13–15 |
| 2:30 – 3:15 | Data Visualization + Insights | 16 |
| 3:15 – 4:15 | 🚀 Mini Hackathon | 17–20 |
| 4:15 – 4:30 | Demo + Wrap-Up | 21–25 |

---

---

# ⏰ 9:30 – 10:00 | KICKOFF + IoT MINDSET

🔥 **Energy level: HIGH** — Room is fresh. Start with a game. No slides yet.

---

## ▶ SLIDE 1 — Title Slide

### Opening — Don't Say Hello

> 💡 **TIP:** Walk in confidently. Don't say good morning. Don't introduce yourself yet. Open with the question instead — it hooks the room immediately before they've had a chance to zone out.

---

🎤 **SAY THIS:**

> *"Raise your hand if you've ever talked to your fridge."*

Wait. Look around the room. Let a few hands go up. Nod slowly.

> *"Raise your hand if your fridge has ever talked back."*

Pause for 3 full seconds. Let them laugh or look confused.

> *"...That's IoT. And by 4:30 today, you'll know exactly how that fridge thinks, what it senses, and how it sends that data to your phone. Let's get into it."*

Now introduce yourself. Keep it to one sentence — your name, your background. Then move on immediately.

---

## 🎮 GAME 1 — IoT or NOT IoT?

> **Time:** 3–4 minutes  
> **No slides needed. Just your voice.**

🎤 **SAY THIS:**

> *"Before we touch any code — let's calibrate your brain. I'm going to describe something. You shout IoT or NOT IoT. Fast. Ready? GO."*

Point at students randomly for answers. Be dramatic about wrong answers.

| You say | Answer | What to add |
|---|---|---|
| "A light bulb that turns on when you enter the room" | ✅ IoT | "Built on LDR + relay. ₹200 of components." |
| "A normal ceiling fan with a wall switch" | ❌ NOT IoT | "Boring. No internet. Just physics." |
| "A dustbin in a city that texts the municipality when it's full" | ✅ IoT | "This is real. Singapore does this." |
| "Your grandmother calling you on the landline" | ❌ NOT IoT | "Unless she's on WiFi. Then... maybe." |
| "A cow on a farm with a GPS tag in its ear" | ✅ IoT | "Yes, this is real. Yes, it is weird. Welcome to IoT." |

🎤 **SAY THIS to close the game:**

> *"IoT is basically this: if a thing can gossip about itself on the internet — it's IoT."*

---

## ▶ SLIDE 2 — Full-Day Agenda

Quick walk-through. 30 seconds. Don't read every line — just give them the shape of the day.

🎤 **SAY THIS:**

> *"Here's where we're going today. Morning — we build on ESP32, learn sensors, make LEDs and buzzers do our bidding. Afternoon — we put all of that on the internet with ThingSpeak, visualise live data, and then at 3:15 we build a complete system in one hour. That's the hackathon. That's the payoff. Everything before 3:15 is preparation for that moment."*

---

## ▶ SLIDE 3 — What Is IoT?

### Teaching: What Is IoT?

🎤 **SAY THIS:**

> *"IoT stands for Internet of Things. Simple definition: physical devices that collect data from the real world, connect to the internet, and take action based on that data. Three words — Physical. Connected. Intelligent."*

> *"The keyword is THINGS. Not computers. Not phones. THINGS. Your AC. A parking meter. A hospital wristband. A cow. A dustbin. Any physical object — connected to the internet — becomes an IoT device."*

---

## ▶ SLIDE 4 — IoT Is Already Around You

Quick fire — spend about 20 seconds per card. For each example add one line students recognise:

- **Smart Home** → *"Every Alexa, every Google Nest, every Philips Hue bulb. IoT."*
- **Healthcare** → *"Your Apple Watch measuring heart rate right now. IoT."*
- **Agriculture** → *"Israeli farms use soil sensors. 40% less water. IoT."*
- **Industry 4.0** → *"BMW factories — machines alert maintenance before they break. IoT."*
- **Smart Cities** → *"Barcelona smart parking. Your phone shows empty spots. IoT."*
- **Security** → *"Every smart CCTV camera that sends alerts. IoT."*

🎤 **SAY THIS:**

> *"Every single one of these systems — at the core — is doing the same thing. Reading a sensor, running some logic, sending data somewhere. That pipeline is what you're going to build today."*

---

## ▶ SLIDE 5 — The IoT Pipeline

### Teaching: The Pipeline (Most Important Slide)

> 💡 **TIP:** This is the anchor for the entire workshop. Every time students build something today, bring them back to this: *"Where in the pipeline does this fit?"* Write it on the board if possible.

🎤 **SAY THIS:**

> *"This is the most important slide in this workshop. Write it down. Remember it. Tattoo it. I don't care. But remember it.*
>
> *Sensor → ESP32 → Internet → Cloud → Dashboard → Action.*
>
> *EVERY IoT system ever built follows this exact pipeline. A ₹200 temperature sensor in a student lab. A ₹2 billion Tesla on the highway. Same. Pipeline."*

> *"Think of it like a WhatsApp forward. Something happens in the real world — the sensor notices it. The ESP32 is the aunty who processes it and decides what to do. The internet is the forward button. The cloud is the group chat. The dashboard is you reading it at 2 AM. The action is you actually doing something about it."*

Wait for the laughter to die down.

> *"Sensors are Eyes. ESP32 is the Brain. Cloud is Memory. Dashboard is Voice. Keep that in your head for the rest of the day."*

---

---

# ⏰ 10:00 – 11:00 | ESP32 DEEP DIVE — GPIO & PWM

🔥 **Energy level: HIGH** — Hands-on starts here. Don't lecture for more than 5 minutes without giving them something to do.

---

## ▶ SLIDE 6 — Why ESP32? Not ESP8266?

🎤 **SAY THIS:**

> *"Before we write a single line of code, you need to know WHY we're using ESP32. Because the whole market still uses both, and your future employer might ask."*

> *"ESP8266 is like a Nokia 3310. Reliable. Loved by grandparents. Cannot run Instagram. One core, 80 MHz, only WiFi, 80 KB of RAM. It will blink an LED. That's about it."*

> *"ESP32 is your current phone. Dual core, 240 MHz, WiFi AND Bluetooth, 520 KB RAM, 34 GPIO pins. And it costs ₹200. For two hundred rupees you get a dual-core wireless computer. That's absurd. That's why we use it."*

> 💡 **TIP:** If anyone asks about ESP32-S2 or ESP32-C3 variants — acknowledge them, say those are more recent variants optimised for specific use cases, and that ESP32 classic is still the industry standard for learning.

---

## ▶ SLIDE 7 — GPIO, PWM & Digital Control

### Teaching: GPIO

🎤 **SAY THIS:**

> *"GPIO means General Purpose Input Output. Each pin can be configured to do different things. You decide."*

> *"OUTPUT: You tell the pin — go HIGH. 3.3 volts flow out. An LED lights up. You're the boss.*
>
> *INPUT: You ask the pin — what's happening out there? It tells you. Button pressed? Yes. PIR triggered? Yes. You're still the boss."*

### Teaching: PWM

🎤 **SAY THIS:**

> *"Now PWM. Pulse Width Modulation. Here's the problem — ESP32 is digital. It can only output 0 volts or 3.3 volts. Nothing in between. But what if we want half brightness on an LED? We can't output 1.65 volts. So we cheat."*

> *"We turn the pin ON and OFF so fast — 5000 times per second — that the LED THINKS it's getting half power. It's basically lying to the LED. Very effectively. That's PWM. And that's how your phone controls screen brightness, how a drone controls motor speed, how a servo knows where to point."*

> 💡 **Punchline:** *"PWM: Making LEDs believe a lie — at 5000 Hz."*

---

## ▶ SLIDE 8 — Your First ESP32 Programs

🎤 **SAY THIS:**

> *"Okay. Open your laptops. Go to Wokwi.com. W-O-K-W-I. Not Wikipedia. Wokwi. Free browser-based ESP32 simulator. No hardware. No breadboard. No burnt fingers. No budget."*

Give 2 minutes for everyone to open Wokwi. Walk around. Help anyone lost.

---

### Activity 1 — LED Blink (5 min)

🎤 **SAY THIS:**

> *"First program. Everyone type this. This is the Hello World of hardware."*

```cpp
void setup() {
  pinMode(2, OUTPUT);
}
void loop() {
  digitalWrite(2, HIGH);
  delay(250);
  digitalWrite(2, LOW);
  delay(250);
}
```

Let them run it. Celebrate when the LED blinks. Then say:

🎤 **SAY THIS:**

> *"You just told a microcontroller what to do. That's embedded programming. You're embedded engineers now. Barely. But still."*

---

### Activity 2 — Button to LED (5 min)

🎤 **SAY THIS:**

> *"Now wire a button. Press it — LED turns on. Release — it turns off. That's INPUT controlling OUTPUT. The fundamental loop of all embedded systems."*

```cpp
void setup() {
  pinMode(2, OUTPUT);
  pinMode(15, INPUT_PULLUP);
}
void loop() {
  int btn = digitalRead(15);
  if (btn == LOW) {
    digitalWrite(2, HIGH);
  } else {
    digitalWrite(2, LOW);
  }
}
```

---

### Activity 3 — PWM Auto-Fade (5 min)

🎤 **SAY THIS:**

> *"Now the interesting one. Your LED is going to breathe — fade from off to full brightness and back. Like a MacBook sleep indicator. Except you built it."*

```cpp
void setup() {
  ledcSetup(0, 5000, 8);
  ledcAttachPin(2, 0);
}
void loop() {
  for (int i = 0; i <= 255; i++) {
    ledcWrite(0, i);
    delay(8);
  }
  for (int i = 255; i >= 0; i--) {
    ledcWrite(0, i);
    delay(8);
  }
}
```

---

## 🎮 GAME 2 — Speed Blink Challenge

> **Time:** 3–4 minutes

🎤 **SAY THIS:**

> *"Okay. First person to set their LED blink to EXACTLY 250ms interval — not 200, not 300, exactly 250 — and show it to me running — wins eternal respect."*

Start a countdown on your phone. Call out updates: *"10 seconds... 5... 3... 2..."*

**What to watch for:**
- Students who change `delay(1000)` to `delay(250)` → correct ✅
- Students who try `millis()` → impressive, mention it out loud
- Students stuck → hint: *"the number inside delay() is milliseconds"*

Celebrate the winner loudly. Ask them to explain what they changed.

---

---

# ⏰ 11:00 – 11:15 | ☕ BREAK

🎤 **SAY THIS as they leave:**

> *"Pro tip: IoT engineers only take 15-minute breaks. Set a timer. If you're late back, you owe the group a live sensor demo."*

> 💡 **TIP:** Use the break to walk around and check every student's Wokwi setup. Make sure everyone has LED blink working before moving to sensors. The next session builds on this foundation. Also eat something — the afternoon is intense.

---

---

# ⏰ 11:15 – 12:45 | 🔥 SENSOR PLAYGROUND

🔥 **Energy level: PEAK** — This is the sweet spot. Hit your hardest material here.

---

## ▶ SLIDE 9 — 5 Sensors. 5 Challenges.

🎤 **SAY THIS:**

> *"This is the most important hour of the workshop. You're going to meet five sensors. Each one does something different. Each one is inside a real product you use every day. By the end of this session, you'll know how to wire them, read them, and write logic that responds to them."*

> *"Before we start — remember the pipeline. Sensor is the Input. ESP32 is the Brain. Output is the Decision. Every exercise today follows that structure. Keep asking: what is the input, what is the condition, what is the output?"*

---

## 🎮 GAME 3 — Sensor Bingo

> **Runs throughout the entire sensor session (90 minutes)**

**Setup:** Write these challenge squares on the whiteboard or distribute printed cards.

```
┌──────────────────────┬──────────────────────┬──────────────────────┐
│  Read temp > 35°C    │  Detect motion < 1s  │  Measure dist < 10cm │
├──────────────────────┼──────────────────────┼──────────────────────┤
│  LED on via LDR      │  PWM at exact 50%    │  Print custom alert  │
├──────────────────────┼──────────────────────┼──────────────────────┤
│  Humidity < 50%      │  No motion for 5s    │       FREE           │
└──────────────────────┴──────────────────────┴──────────────────────┘
```

**Rules:** Complete a full row (horizontal, vertical, diagonal) = winner. Students shout "BINGO!" and must show working code to claim it. This keeps everyone engaged even during sensors you're not currently teaching.

---

## ▶ SLIDE 10 — Sensor #1: DHT11

### Temperature & Humidity

🎤 **SAY THIS:**

> *"DHT11. This sensor is inside every smart AC system you've ever used. Costs ₹30. Measures temperature and humidity. Cheap, slow, perfect for learning."*

> *"Here's the key concept: we're not just reading a number. We're making a DECISION based on that number. That's the difference between a dumb sensor and an IoT device. The threshold condition is where the intelligence lives."*

```cpp
#include <DHT.h>
#define DHTPIN 4
#define DHTTYPE DHT11
DHT dht(DHTPIN, DHTTYPE);

void setup() {
  Serial.begin(9600);
  dht.begin();
}

void loop() {
  float temp = dht.readTemperature();
  float hum  = dht.readHumidity();

  if (temp > 30) {
    Serial.println("🔥 HEAT ALERT! Check cooling.");
  }

  Serial.print("Temp: "); Serial.println(temp);
  Serial.print("Hum:  "); Serial.println(hum);
  delay(2000);
}
```

🎤 **SAY THIS:**

> *"Walk through that if-statement. That ONE line is the intelligence of a smart AC thermostat. One condition. One action. Now scale it to a building with 200 sensors — that's a smart HVAC system. IoT is just this, at scale."*

**Student challenges:**
- Change threshold to 25°C. What happens?
- Add `else` — print *"Temperature OK"* when below threshold
- Add a second alert: if humidity > 70, print *"Too humid!"*

---

## ▶ SLIDE 11 — Sensor #2: LDR

### Light Detection

🎤 **SAY THIS:**

> *"LDR stands for Light Dependent Resistor. As light increases, resistance decreases. It's the introvert of sensors — it opens up in the dark."*

> *"Practical use: automatic street lights. High light → high resistance → light OFF. Low light → low resistance → light ON. Same sensor is in your phone adjusting screen brightness."*

```cpp
void loop() {
  int val = analogRead(A0);  // 0 = bright, 4095 = dark

  if (val < 500) {
    digitalWrite(LED_PIN, HIGH);  // dark → LED ON
  } else {
    digitalWrite(LED_PIN, LOW);   // light → LED OFF
  }
  delay(100);
}
```

**Student challenge:** Add `Serial.println(val)` to print the raw reading. Watch what changes when you cover it vs shine a light at it.

---

## ▶ SLIDE 11 — Sensor #3: HC-SR04 Ultrasonic

### Distance Measurement

🎤 **SAY THIS:**

> *"Bats navigate using ultrasound. They emit a pulse, it bounces off objects, they measure the echo time, they know the distance. This sensor does exactly the same thing — minus the rabies."*

> *"This exact sensor is in your car's parking assist system. The beeping that gets faster as you approach a wall? That's a for-loop with a decreasing delay. You're going to build that right now."*

```cpp
#define TRIG_PIN 5
#define ECHO_PIN 18

void loop() {
  digitalWrite(TRIG_PIN, HIGH);
  delayMicroseconds(10);
  digitalWrite(TRIG_PIN, LOW);

  long duration = pulseIn(ECHO_PIN, HIGH);
  long distance  = duration / 58;  // convert to cm

  Serial.print("Distance: ");
  Serial.print(distance);
  Serial.println(" cm");
  delay(500);
}
```

> 💡 **TIP — Why 58?** Sound travels at ~343 m/s. `pulseIn()` returns microseconds for a round trip. Distance = (duration / 2) / 29.1 = duration / 58. Students often ask — this is the answer.

**Student challenge:** Print *"DANGER!"* if distance < 10 cm. Add an LED that turns on when something is close.

---

## ▶ SLIDE 12 — Sensor #4: PIR

### Motion Detection

🎤 **SAY THIS:**

> *"PIR stands for Passive Infrared. It detects heat moving across its field of view. Not just heat — MOVING heat. A warm wall doesn't trigger it. A person walking across does."*

> *"You know those hotel bathroom lights that turn off while you're still in there? Badly calibrated PIR with a short timeout. Today you'll build a better one."*

> *"PIR is passive — it doesn't emit anything. It just listens. Like a very judgemental security guard who says nothing until you move."*

```cpp
#define PIR_PIN 13
#define LED_PIN 2

void loop() {
  if (digitalRead(PIR_PIN) == HIGH) {
    Serial.println("⚠️ Motion Detected!");
    digitalWrite(LED_PIN, HIGH);
    delay(3000);           // stay on for 3 seconds
    digitalWrite(LED_PIN, LOW);
  }
}
```

**Student challenge:** Add a counter — track how many motion detections per minute. Print *"High traffic area!"* if count > 5.

---

## ▶ SLIDE 12 — Sensor #5: Potentiometer

### Analog Control

🎤 **SAY THIS:**

> *"This is the analog knob. You turn it, a wiper moves across a resistive track, voltage at the output changes from 0 to 3.3V. ESP32 reads that as 0 to 4095."*

> *"This is how an old radio volume knob works. Except now instead of audio signal, you're controlling LED brightness. Rotate left — LED dims. Rotate right — LED brightens. Simple. Satisfying. Fundamental."*

```cpp
void setup() {
  ledcSetup(0, 5000, 8);
  ledcAttachPin(2, 0);
}

void loop() {
  int val  = analogRead(35);         // 0–4095
  int duty = map(val, 0, 4095, 0, 255);
  ledcWrite(0, duty);
  delay(10);
}
```

---

---

# ⏰ 12:45 – 1:30 | 🍽️ LUNCH BREAK

🎤 **SAY THIS before they leave:**

> *"Lunch break. Come back full, awake, and with at least one project idea already forming in your head. Seriously — start thinking now. You'll thank me at 3:15."*

> 💡 **TIP:**
> - Walk around and note who finished all 5 sensor challenges
> - Note who is struggling — pair them with stronger students in the afternoon
> - Think about hackathon team pairings (ideally 2–3 students each)
> - Eat something — the afternoon is the most intense part

---

---

# ⏰ 1:30 – 2:30 | NETWORKING + THINGSPEAK CLOUD

😴 **Energy level: POST-LUNCH DIP** — Open with the pipeline question to activate brains. Do NOT start with a lecture.

---

## ▶ SLIDE 13 — How ESP32 Talks to the World

### Hook — One Question First

🎤 **SAY THIS:**

> *"Quick question before we start. What's the difference between the sensor data you built this morning — sitting in your Serial Monitor — and a real IoT product?"*

Wait for answers. Students will say: app, internet, cloud, dashboard. Guide toward:

> *"The answer is one word: the internet. Right now your data lives inside your laptop. Nobody else can see it. You can't check it on your phone. It can't trigger alerts. It's a sensor reading trapped in a box.*
>
> *Today we give it wings."*

---

### Teaching: WiFi on ESP32

🎤 **SAY THIS:**

> *"ESP32 has WiFi built in. No extra module. No shield. No additional cost. Here's the entire WiFi connection code:"*

```cpp
WiFi.begin("YOUR_WIFI_NAME", "YOUR_PASSWORD");

while (WiFi.status() != WL_CONNECTED) {
  delay(500);
}
Serial.println("Connected! IP: " + WiFi.localIP().toString());
```

> *"That's it. Three lines. Your ESP32 is now a node on the internet. Please use this responsibly."*

---

### Teaching: HTTP vs MQTT

🎤 **SAY THIS:**

> *"How does data travel? Two main protocols in IoT."*

> *"HTTP is like a polite conversation. You knock on the server door. Server opens. You say your thing. You leave. Server responds. Request-response. Fine for most things. Slightly slow for real-time."*

> *"MQTT is like turning on notifications for your favourite YouTuber — except the YouTuber is a temperature sensor. You subscribe to a topic. Whenever data changes, you get it instantly. No knocking. Just push. This is what Tesla cars use. This is what smart factories use. Less data, lower latency, perfect for IoT."*

> *"Today we use HTTP because it's easier to see what's happening. But know that MQTT is the industry standard for production IoT systems."*

---

## ▶ SLIDE 14 — ThingSpeak: Your Free IoT Cloud

### Teaching: ThingSpeak

🎤 **SAY THIS:**

> *"ThingSpeak is a cloud platform built specifically for IoT data. Made by MathWorks — same company that makes MATLAB. Big company. Proven platform. Free tier that's more than enough for everything we're doing today."*

> *"Three things to know:*
>
> *A CHANNEL is your data container — like a WhatsApp group dedicated to your sensor. Only your ESP32 posts there.*
>
> *A FIELD is one type of data inside that channel. Field 1 is temperature. Field 2 is humidity. You can have up to 8 fields per channel.*
>
> *The WRITE API KEY is your secret password. Your ESP32 uses it to post data. Nobody else should have it."*

> 💡 **TIP:** Write on the board: **WRITE KEY = your ESP32 SENDS data. READ KEY = apps and dashboards READ data.** This distinction catches almost everyone the first time.

### Live Setup — Do This Together on Projector

1. Go to **thingspeak.com** → Sign Up Free
2. Click **New Channel** → Name it *"ESP32 Weather Station"*
3. Field 1: `Temperature` — Field 2: `Humidity` → **Save Channel**
4. Go to **API Keys** tab → **Copy the Write API Key**
5. Paste it into the code below

---

## ▶ SLIDE 15 — Uploading DHT11 → ThingSpeak

### Live Code: DHT11 → ThingSpeak

🎤 **SAY THIS:**

> *"Now watch me walk through this URL — because this is not magic. This is just a web address. Your browser opens URLs every day. Your ESP32 is doing the same thing, except instead of loading a webpage, it's POSTING data to a database."*

```cpp
#include <WiFi.h>
#include <HTTPClient.h>
#include <DHT.h>

const char* ssid = "WiFi_Name";
const char* pass = "WiFi_Pass";
String apiKey    = "PASTE_YOUR_WRITE_KEY_HERE";

#define DHTPIN 4
#define DHTTYPE DHT11
DHT dht(DHTPIN, DHTTYPE);

void setup() {
  Serial.begin(115200);
  dht.begin();
  WiFi.begin(ssid, pass);
  while (WiFi.status() != WL_CONNECTED) { delay(500); }
  Serial.println("WiFi Connected!");
}

void loop() {
  float t = dht.readTemperature();
  float h = dht.readHumidity();

  if (!isnan(t) && !isnan(h)) {
    String url = "http://api.thingspeak.com/update"
                 "?api_key=" + apiKey
                 + "&field1=" + String(t)
                 + "&field2=" + String(h);

    HTTPClient http;
    http.begin(url);
    int code = http.GET();  // returns entry ID (1, 2, 3...)
    Serial.println("Upload Code: " + String(code));
    http.end();
  }

  delay(20000);  // ThingSpeak free tier: max 1 update per 15 sec
}
```

### Break Down the URL Live

🎤 **SAY THIS:**

> *"Look at this URL. `api.thingspeak.com/update` — that's the endpoint. The question mark starts the parameters. `api_key=` is the password. `&field1=` is the temperature value. `&field2=` is humidity.*
>
> *You're not doing anything complicated. You're opening a URL. ThingSpeak validates the key, stores the data, and draws a chart. That's all of IoT at the HTTP level."*

> *"When ThingSpeak accepts your data, it sends back the entry ID — the number 1, 2, 3 counting your uploads. Positive number = it worked. `-1` = WiFi broken. `400` = wrong API key."*

> *"This `delay(20000)` at the bottom — 20 seconds. ThingSpeak free tier allows one update every 15 seconds. We use 20 to be safe. In production, you think carefully about this: too frequent wastes bandwidth and battery, too slow means stale data."*

---

## 🎮 GAME 4 — Who Uploaded First?

> **Time:** 5 minutes

🎤 **SAY THIS:**

> *"Everyone set up your ThingSpeak channel and paste your API key into the code. First team to show me a LIVE ThingSpeak graph with at least 3 data points — wins."*

**Common errors and fixes:**

| Error | Cause | Fix |
|---|---|---|
| WiFi never connects | Wrong SSID/password | Case-sensitive — double check |
| Upload Code: -1 | No internet | Try mobile hotspot |
| Upload Code: 400 | Wrong API key | Re-copy from ThingSpeak, no spaces |
| Graph shows 0 values | DHT not reading | Check Wokwi pin connections |
| Graph not updating | Sending too fast | Increase `delay()` to `20000` |

> 💡 **TIP:** Project your own ThingSpeak channel on screen so students can see what a healthy live graph looks like before they have their own working.

---

---

# ⏰ 2:30 – 3:15 | DATA VISUALIZATION + INSIGHTS

⚡ **Energy level: MEDIUM** — Settling in after the ThingSpeak excitement. The anomaly game creates a spike of engagement right when you need it.

---

## ▶ SLIDE 16 — From Raw Data to Real Insights

### Hook — The Grocery Receipt

🎤 **SAY THIS:**

> *"Raw data is like a grocery receipt. All the information is technically there. But nobody reads it. Nobody looks at a receipt and thinks: I should optimise my spending this week.*
>
> *A dashboard turns your data into a story. A story with a beginning, a middle, and an alarm."*

---

### Teaching: What ThingSpeak Can Do

🎤 **SAY THIS:**

> *"Real-time charts — your sensor is plotting its own graph right now. No Excel. No Python. Just data showing up as it happens."*

> *"Anomaly detection — see that spike at 3AM? That's not normal temperature variation. That's a server overheating at night when no one is watching. A dashboard makes it obvious. Raw numbers hide it."*

> *"ThingSpeak React — my favourite feature. Set a rule: if Field 1 goes above 35 degrees, send me an email. No code. Just a form. Free automated alert system. That is IoT doing its actual job."*

> *"Dashboard design — when you combine a temperature gauge, a humidity chart, a motion log, and an alert history into one view — that's a product. That's something a company would pay for."*

---

## 🎮 GAME 5 — Spot the Anomaly

> **Time:** 10 minutes

**Setup:** Draw or project this dataset on screen — 24 hours of server room temperature, roughly 22–25°C most of the time, with one clear event:

```
Time:  00:00  01:00  02:00  03:00  03:30  04:00  08:00  12:00
Temp:    23     23     24     48     51     49     24     25
```

🎤 **SAY THIS:**

> *"Here is 24 hours of temperature data from a server room. I've been called to investigate. Something happened. You have 2 minutes. Discuss with the person next to you. What happened, when, and what should have been done?"*

Wait 2 minutes. Take 3 answers from the room. Then reveal:

🎤 **SAY THIS:**

> *"At 3AM the AC in the server room shut off. Temperature spiked to 51 degrees in 30 minutes. Two servers crashed by morning.*
>
> *If they had set a ThingSpeak React alert at 35 degrees — the on-call engineer would have been emailed at 3:04 AM. They found out at 8AM when staff arrived.*
>
> *That's why dashboards exist. Not to look pretty. To catch problems before they become disasters. In IoT, a chart is not decoration. A chart is an alarm you haven't set yet."*

---

---

# ⏰ 3:15 – 4:15 | 🚀 MINI HACKATHON

🔥 **Energy level: HIGH** — Play hype music. Walk around constantly. Do NOT sit down during this session.

---

## ▶ SLIDE 17 — Build a Complete IoT System!

### Launch — Setting the Stakes

🎤 **SAY THIS:**

> *"Okay. Stop everything. Close your notes. This is it. This is the session you've been building toward all day."*

> *"In the next 60 minutes you're going to build a complete IoT system. End to end. Sensor reading real data. ESP32 making a decision. Logic conditions. At least a simulation of data going to the cloud."*

**Three requirements — put on slide or board:**
1. ≥ 2 sensors used
2. Logic conditions — at least one `if/else`
3. Cloud simulation (real ThingSpeak upload OR this in your code):

```cpp
Serial.println("Uploading to ThingSpeak: field1=" + String(sensorValue));
Serial.println("HTTP Response: 200 OK");
```

🎤 **SAY THIS:**

> *"At 4:15 every team demos for two minutes. I will ask exactly one follow-up question. The three questions I always ask are: What does it do? How does it work? Where does the data go? Practice those answers while you build."*

---

### Project Options

🎤 **SAY THIS — read these out one by one:**

> *"Option A: Smart Room Automation. LDR + PIR + LED. Classic. The sensor combo powering every smart building on this planet. Light only turns on when it's dark AND someone is present. Energy efficient. Real product."* — **(Slide 18)**

> *"Option B: Smart Parking System. Ultrasonic detects car presence, logs occupancy."*

> *"Option C: Smart Weather Station. DHT11 + live ThingSpeak graph + temperature alert."* — **(Slide 19)**

> *"Option D: Smart Security System. PIR triggers buzzer and alert message."*

> *"And for the brave ones — the Assistive Smart Helmet. Multi-sensor. Custom alert logic. This one stands out in a portfolio. This is your Iron Man suit — if Iron Man was made with 500 rupees of components."*

---

### Your Role During the Hackathon

> 💡 **TIP — Be a coach, not a debugger:**
>
> ❌ **Wrong:** *"Here is the fix to your code."*  
> ✅ **Right:** *"What is your sensor reading right now? ... What should happen if it's above that? ... Write that as an if-statement."*
>
> Walk around every 5 minutes. Don't let anyone sit idle for more than 3 minutes without checking in. Play background music — it reduces stress and helps focus. Pair struggling students with ones who finished early.

---

## 🎮 GAME 6 — Wildcard Component

> **For fast finishers only**

🎤 **SAY THIS when a team finishes:**

> *"Congratulations. You get a wildcard. Choose one:*
>
> *A: Add a buzzer that sounds when your threshold is crossed*  
> *B: Add an OLED display showing live sensor readings*  
> *C: Add a third sensor you haven't used today*
>
> *20 bonus creativity points. You have the rest of the hackathon."*

This keeps strong students challenged while you focus on helping others catch up.

---

## ▶ SLIDE 20 — Judging Criteria

As you walk around, mentally score each team:

| Criteria | Points | What to look for |
|---|---|---|
| Logic & Code | 30 | Does it work? Are conditions clean? Is it readable? |
| Creativity | 30 | Interesting problem? Did they go beyond the brief? |
| Real-World Value | 25 | Could this actually solve something for real people? |
| Demo & Explanation | 15 | Can they explain it clearly in 2 minutes? |

---

---

# ⏰ 4:15 – 4:30 | DEMO + WRAP-UP

⚡ **Energy level: MEDIUM** — Slow the room down. Be genuine. This is the moment they remember.

---

## ▶ SLIDE 21 — How the Demo Works

🎤 **SAY THIS:**

> *"Okay teams — demo time. Each team has two minutes. Show me your simulation running. Tell me what it does. I'll ask one question. That's it. Let's go."*

**For each demo — give specific, genuine feedback. Not generic "nice work":**
- *"The threshold condition here is smart — you didn't just print an alert, you designed an actual rule. That's real engineering."*
- *"Adding a third sensor in 45 minutes and it still works — that's product thinking."*
- *"The fact that your Serial Monitor output is readable and informative — that's professional."*

> 💡 **TIP — The best follow-up question to ask every team:**  
> *"If you were deploying this in the real world — what would break first?"*  
> This forces systems thinking and treats them as engineers, not students.

---

## ▶ SLIDE 22 — The Building Blocks of IoT

### Recap — The Full Picture

🎤 **SAY THIS:**

> *"Before I wrap up, let's look at what you built today. Not what you learned. What you BUILT."*

> *"This morning you started by blinking an LED. Embarrassingly simple. By lunchtime you had five sensors talking to an ESP32, making decisions, triggering outputs.*
>
> *This afternoon you put that sensor data on the internet. You created a live dashboard that any phone in the world can see. You set alerts. You detected anomalies.*
>
> *And then you built a complete system — from scratch — in one hour."*

---

## ▶ SLIDE 23 — IoT Is a Career, Not a Hobby

🎤 **SAY THIS:**

> *"I want to tell you something important before you leave. IoT is not a hobby project. The IoT market is growing at 25% per year. Smart cities, precision agriculture, healthcare monitoring, predictive maintenance, connected vehicles — all of it runs on what you learned today."*

> *"The skills you used — GPIO programming, sensor integration, REST APIs, cloud dashboards — these are exactly what embedded engineers, IoT cloud architects, and product engineers get hired for. These are not beginner skills. These are industry skills."*

---

## ▶ SLIDE 24 — Keep Building After Today

🎤 **SAY THIS:**

> *"You can replicate everything from today for under 500 rupees. ESP32 is 250. DHT11 is 30. Ultrasonic is 50. PIR is 40. LDR is 10. Total: 380 rupees. One weekend. One breadboard. You can build every project from today on real hardware."*

> *"Wokwi is free forever for simulation. ThingSpeak is free forever for 4 channels. Random Nerd Tutorials has free guides for every sensor you can imagine. There are zero excuses to stop building."*

---

## ▶ SLIDE 25 — YOU DID IT! 🎉

### The Closing

🎤 **SAY THIS:**

> *"Most people who learn programming stop at making things work on a screen. You built systems that interact with the real world today. You built things that read the environment, make decisions, and respond automatically. That is not basic programming. That is embedded systems. That is IoT engineering."*

> *"You are not beginners anymore."*

**Pause. Let it land. Then:**

> *"You're dangerous. In the best way."*

---

### Exit Ticket — Every Person Answers

🎤 **SAY THIS:**

> *"Before you go — one question, each person. No laptop needed. Just one answer. Pick any one of these three:*
>
> *One: Name one sensor and the real-world product you'd build with it.*  
> *Two: What's the one thing you'd learn next to go deeper in IoT?*  
> *Three: If I gave you 1000 rupees and a weekend — what would you build?"*

Go around the room. Every person answers. Don't skip anyone. These answers tell you what resonated — and they cement the learning for the students themselves.

---

---

# 📎 APPENDIX

---

## Energy Management by Hour

| Time | Energy | What to Do |
|---|---|---|
| 9:30 AM | 🥶 Cold | Start with the fridge game. No slides. Get them laughing. |
| 10:00 AM | 🔥 Warming | First hands-on. Keep challenges short. Celebrate wins loudly. |
| 11:15 AM | 🔥🔥 Peak | Fire the hardest sensor material here. This is the sweet spot. |
| 12:45 PM | 😴 Pre-lunch | End with a funny line. Release them on time. |
| 1:30 PM | 😴 Post-lunch | Use the anomaly question FIRST. Don't lecture cold. |
| 2:30 PM | ⚡ Settling | Anomaly game works perfectly. Active thinking, not passive listening. |
| 3:15 PM | 🚀 Adrenaline | Play hype music. Walk around constantly. |
| 4:15 PM | 😌 Tired but proud | Slow down. Be genuine. This is what they remember. |

---

## Common Student Errors & Fixes

| Error | Cause | Fix |
|---|---|---|
| LED doesn't blink | Wrong pin number | ESP32 built-in LED is pin 2. Check wiring in Wokwi. |
| DHT11 reads `NaN` | Wrong pin defined | Check DHTPIN matches your Wokwi wiring. |
| WiFi never connects | Wrong SSID/password | Case-sensitive. Use Wokwi's built-in WiFi for simulation. |
| ThingSpeak returns `-1` | No internet | Verify `api.thingspeak.com` is reachable. |
| ThingSpeak returns `400` | Wrong API key | Re-copy from ThingSpeak API Keys tab. No spaces or extra characters. |
| ThingSpeak graph shows flat 0 | DHT read failing silently | Add `Serial.println(temp)` before the URL to see raw values. |
| Ultrasonic always 0 cm | TRIG and ECHO swapped | Check wiring and that pin defines match your code. |
| PIR never triggers | Sensitivity in simulator | In real hardware, adjust the pot on the back of the sensor. |
| PWM LED always full brightness | `ledcSetup()` missing | Channel number in `ledcSetup()`, `ledcAttachPin()`, and `ledcWrite()` must all match. |
| Code compiles but nothing in Serial | Baud rate mismatch | `Serial.begin(9600)` in code → open monitor at 9600 baud. |

---

## Bonus Game A — What Sensor Fixes This?

Read out the problem. Students name the sensor.

| Problem | Sensor |
|---|---|
| Street lights stay on in daylight | LDR |
| AC runs when nobody's in the room | PIR |
| You don't know the warehouse is flooding | Ultrasonic / Water sensor |
| Your grandma's house overheats and nobody checks | DHT11 |
| Car park looks full but you can't tell from outside | Ultrasonic |
| Parcels left in the sun are getting heat-damaged | DHT11 + LDR combo |

---

## Bonus Game B — ESP32 Trivia

Quick fire. 10 seconds per question. Raise hand to answer.

| Question | Answer |
|---|---|
| How many cores does ESP32 have? | 2 (dual core) |
| What voltage does GPIO output at HIGH? | 3.3V |
| What does GPIO stand for? | General Purpose Input Output |
| What does PWM stand for? | Pulse Width Modulation |
| HTTP or MQTT — which is better for real-time IoT? | MQTT |
| What ThingSpeak feature emails you when data crosses a threshold? | React |
| How many fields per channel on ThingSpeak free tier? | 8 |
| Minimum delay between ThingSpeak updates (free)? | 15 seconds |

---

*End of Script*

*You've got this. Have fun. They'll remember the instructor more than the slides. 🚀*
