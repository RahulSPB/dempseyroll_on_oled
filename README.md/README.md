# 🥊 Dempsey Roll Animation on OLED using ESP32

This embedded project displays a **frame-by-frame animation of Makunouchi Ippo's Dempsey Roll** from *Hajime no Ippo* on a **0.96" 128x64 I2C OLED display** using an **ESP32** board. The animation simulates the iconic boxing move with clean bitmap transitions.

---

## 📸 Preview

> *(Insert OLED photo or animated GIF of the screen here)*

---

## 📦 Features

- ⬛ **Monochrome OLED animation** (128×64 resolution)
- 🧠 Uses **frame buffers** and bitmaps for motion simulation
- 🔁 Smooth looping of boxing sequence (Dempsey Roll)
- ⚡ Lightweight and optimized for ESP32 + SSD1306
- 🔧 Designed with expandable support for audio, sensors, or input triggers

---

## 🛠️ Hardware Required

| Component           | Description                         |
|--------------------|-------------------------------------|
| ESP32 Dev Board    | Any common ESP32 development board  |
| OLED Display       | 128x64 I2C (SSD1306-based)          |
| Jumper Wires       | For I2C connections                 |
| (Optional) Button  | To trigger animation manually       |

---

## 🔌 Wiring (I2C)

| OLED Pin | ESP32 Pin (Default) |
|----------|---------------------|
| GND      | GND                 |
| VCC      | 3.3V                |
| SDA      | GPIO 21             |
| SCL      | GPIO 22             |

> ⚠️ Use 3.3V for VCC to avoid over-volting the OLED.

---

## 📂 Project Structure

```plaintext
📁 DempseyRoll_OLED/
 ┣ 📄 README.md
 ┣ 📄 dempsey_roll.ino         
 ┣ 📄 docs
 ┣ 📄 converted_bitmaps             
 ┣ 📄 schematics             
 ┣ 📄 photos              
 ┗ 📄 video                

---

## 🧠 How It Works
- Images of Ippo performing the Dempsey Roll are downscaled to 128×64 pixels.

- Each frame is converted to a monochrome bitmap array using image2cpp.

- The sketch cycles through the bitmaps in a loop using:

display.drawBitmap(x, y, frame, width, height, color);

- The delay between frames controls the animation speed.

---

## 🚀 Getting Started
- Clone or download this repo.

- Open dempsey_roll.ino in Arduino IDE or PlatformIO.

- Install required libraries:

Adafruit_SSD1306

Adafruit_GFX

- Upload to ESP32 

---

## 📚 Resources

- image2cpp Bitmap Converter

- Adafruit SSD1306 Docs

---

##🧱 Future Ideas
- 🔊 Add I2S speaker for punch sound

- ⌛ Trigger animation on punch via accelerometer

- 🎮 Build interactive OLED boxing mini-game

- 🧭 Add buttons to switch between animations (KO, Victory, Training Mode)

---

##👤 Author
[Rahul /https://github.com/RahulSPB]




