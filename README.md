# 🎙️ Ariel Voice Generation (Unity Asset)

This is the public documentation repository for Ariel Unity. To download and install the plugin, please log in at: https://create.xandimmersion.com/login?ariel=true

The **Ariel Voice Generation** Unity asset allows you to create high-quality voiceovers from text, either in the **Editor** or directly **at Runtime**. Ideal for both developers and narrative designers, it supports dynamic generation, glossary customization, CSV batch imports, and much more.

> 📄 Full [API Documentation]((https://documenter.getpostman.com/view/15655549/2sAYdfrX6M):  

---

## 🧩 Installation

1. Import the asset into your Unity project
2. (Optional) Open the `DemoScene` to explore a working Runtime setup
3. Start using the **Runtime component** or the **Editor Window**, depending on your workflow

---

## 🚀 Getting Started (Runtime)

### 🗺️ Open the Demo Scene

1. Navigate to `ArielVoiceGeneration/Demo/Scene/`
2. Open `DemoScene.unity`

### 🧩 Set Up Your API Key & Speaker

1. In **`Window > ArielVoiceGeneration`** : paste your **API key**. You can get your API key [here](https://create.xandimmersion.com/ariel) 
2. Select the GameObject with the `ArielVoiceRuntime` script
3. In the **Inspector**: Enter a valid **speaker name** (e.g., `"Abrogail"`)

### ▶️ Trigger Voice Generation

- The button in the UI triggers voice generation and plays the resulting `.wav` audio clip using Unity’s `AudioSource`.

---

## 🎮 Runtime Overview

Use `ArielVoiceRuntime.cs` to generate and play speech during gameplay.

### Script Parameters

| Field              | Description                                  |
|-------------------|----------------------------------------------|
| `apiKey`           | Your Ariel API key                           |
| `selectedSpeakerId`| Speaker ID (e.g., `"Abrogail"`)              |
| `textToGenerate`   | Text to convert into speech                  |
| `temperature`      | Controls randomness (0.0–1.0)                |
| `generateButton`   | UI Button that triggers the generation       |

---

## 🛠️ Editor Window Overview

Open the Editor window via:  
**`Window > ArielVoiceGeneration`**

### 🧪 Generation Tab

| Feature         | Description                                       |
|-----------------|---------------------------------------------------|
| `Text to Speech`| Enter your dialogue or narration                  |
| `Voice`         | Select from available speakers                    |
| `Language`      | Choose a language if the speaker supports several |
| `Volume`        | From -32dB to +32dB                               |
| `Pitch`         | Between -1 and +1                                 |
| `Speed`         | Adjust speed of the generated voice               |
| `Effect`        | Add special audio effects (e.g. "bad reception")  |
| `Output Folder` | Choose where to save the generated `.wav` files  |
| `Save to wav`   | Generate the audio and save it to disk            |

> You can insert pauses directly into text using tags like `<pause 1s>` or `<pause 500ms>`.

### 📄 Import CSV

Import a sentence list from a CSV file to batch-generate lines across multiple channels.

### 📘 Glossary Tab

Customize word pronunciations with a simple CSV format:
word,pronunciation technical,teknikal hero,hii-roh


You can:
- Create new glossaries
- Edit existing glossaries
- Import/export glossary files

---

## 🗣️ Fetching Available Voices

You can retrieve supported speaker names in two ways:

- **Editor Window**: Click `Fetch Speakers` (top-right of the window)
- **Code**: Call `FetchAvailableVoices()` in `ArielVoiceRemote`

> ✅ Example voice: `"Abrogail"`

---

## ❗ Error Handling

| Case                 | What Happens                                |
|----------------------|----------------------------------------------|
| Invalid API Key      | Error in Console: `"Invalid API key"`       |
| Missing Audio Button | Warning on play: `"Generate button not set"`|
| Server/API Failure   | Console shows server error details           |

---

## 🔗 API Reference

Read the full Ariel API spec (authentication, endpoints, error handling, etc.):  
👉 **[API Documentation on Postman](https://documenter.getpostman.com/view/15655549/2sAYdfrX6M)**

---

## 📬 Support & License

- Join the **[X&Immersion discord](https://discord.com/invite/qDMwNCDE8X)** and chat with the technical support
- or per email at [contact@xandimmersion.com](mailto:contact@xandimmersion.com)
- Licensed under the [Unity Asset Store EULA](https://unity.com/legal/as-terms)
- Includes `SavWav.cs` by Calvin Rien (MIT-licensed open source)

---

Thanks for using **Ariel Voice Generation**!  
Let us know how you're using it — from games to dialogue systems, virtual assistants, interactive fiction, or more.


