# 🍳 Cal AI

**Cal AI** is an AI-powered Recipe & Meal Planner app.

The app features a **premium black aesthetic**, inspired by the sleek design of [calai.app](https://www.calai.app/), providing a modern and professional user experience.

This app leverages the **Gemini API** to generate creative recipes, analyze nutritional content, and deliver personalized weekly meal plans based on user preferences.

---

## 📚 Documentation

For detailed documentation on setup, architecture, dependencies, and configuration, see the [docs folder](docs/README.md):

- **[Getting Started](docs/GETTING_STARTED.md)** - Installation and setup
- **[Project Architecture](docs/PROJECT_ARCHITECTURE.md)** - Code structure and design
- **[Dependencies](docs/DEPENDENCIES.md)** - Packages and usage
- **[API Documentation](docs/API_DOCUMENTATION.md)** - Gemini API guide
- **[Configuration Guide](docs/CONFIGURATION.md)** - Customization options

---

## 🚀 Features

### ✅ Login / Sign-Up

- Secure authentication for personalized access.
- Firebase Authentication (Fully integrated for login and signup)

---

### ✅ Recipe Generation

- 📸 **Image Input:** Snap or upload ingredient photos for recipe suggestions.
- 🎙️ **Voice Input:** Speak your recipe request (powered by **Whisper** speech-to-text).
- 💬 **Text Input:** Type ingredient names or custom requests.
- ⚡ **Dietary Filters:** Choose from:
  - None
  - Keto
  - Halal
  - High-Protein
  - Nutritious
- 🍽️ **AI Output:**
  - Auto-generated recipe title
  - Ingredients
  - Steps
  - Nutrition info (visualized as a pie chart via **Calorie AI**)
  - AI-generated recipe images

---

### ✅ Weekly Meal Planner

- 🎯 Personalized 7-day meal plan based on selected dietary filters.
- 🧠 Answer 10 MCQs to fine-tune AI meal suggestions.
- 🗓️ Export your meal plan as a **PDF**.

---

### ✅ Profile Section

- 📊 Tracks the total number of recipes generated.
- 📝 Displays a list of previously generated recipe titles.

---

### ✅ About Section

- ℹ️ App information and developer credits.

---

## 🧠 Tech Stack

| Technology         | Usage                                           |
| ------------------ | ------------------------------------------------ |
| GetX                | State Management                                |
| Firebase Auth       | User Authentication                             |
| Cloud Firestore     | User Profiles & Recipe Persistence              |
| SharedPreferences   | Local Settings Storage                          |
| Gemini API          | AI Recipe, Meal Plan, and Nutrition Generation  |
| Image Picker        | Camera / Gallery Integration                    |
| Printing Package    | PDF Meal Plan Export                            |

---

## 👨‍💻 Developer

**Vishnu**

---

## 🚀 Quick Start

1. **Clone the repository**

    ```bash
    git clone https://github.com/Sethuvishnu/healthyu.git
    cd healthyu
    ```

2. **Install dependencies**

   ```bash
   flutter pub get
   ```

3. **Configure API key**
   - Get a Gemini API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Create a `.env` file in the project root:
     ```
     GEMINI_API_KEY=your_gemini_api_key_here
     ```
   - Keys are loaded at runtime via `flutter_dotenv` and referenced through `lib/config/api_keys.dart` — never hardcoded in source.
   - See [API Documentation](docs/API_DOCUMENTATION.md) for details

4. **Run the app**
   ```bash
   flutter run
   ```

5. **Generate Android APK**
   ```bash
   flutter build apk --release
   ```
   The APK will be available at `build/app/outputs/flutter-apk/app-release.apk`

For detailed instructions, see [Getting Started Guide](docs/GETTING_STARTED.md)

---

## 📂 Project Structure

```
lib/
├── main.dart
├── config/               # Configuration & API keys
├── constants/            # App-wide constants
├── controllers/          # GetX Controllers (State Management)
├── models/               # Data models
├── screens/              # UI screens
├── services/             # API & Firebase services
├── widgets/              # Reusable widgets
└── utils/                # Utilities
```

See [PROJECT_ARCHITECTURE.md](docs/PROJECT_ARCHITECTURE.md) for details.

---

## ⚠️ Notes

- ☁️ **Cloud Database:** Integrated with **Firebase Firestore** for persistent storage.
- 🔒 API keys are loaded from a local `.env` file (git-ignored) and **never hardcoded** in the repository.
- 📁 Organized project structure with clear separation of concerns.
- 🛠️ Ready for continued development.

---

## 🛠️ Development Roadmap

- [ ] Upload any YouTube video and get the ingredients