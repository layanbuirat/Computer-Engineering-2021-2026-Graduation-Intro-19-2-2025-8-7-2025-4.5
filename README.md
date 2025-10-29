Of course! Based on the detailed project report, here is a comprehensive and well-structured `README.md` file you can use for your GitHub repository. It summarizes the project's purpose, features, technology, and structure, making it easy for visitors to understand and use your project.

---

# MealLens: AI-Powered Meal Recognition & Recipe Assistant 🍕🤖

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

**MealLens** is a smart, cross-platform mobile application that bridges the gap between food discovery and meal preparation. Using state-of-the-art computer vision and deep learning, it allows users to identify meals from images and receive personalized, detailed recipes with nutritional and allergen information.

---

## ✨ Key Features

### 🍽️ Core Application Features
*   **AI-Powered Meal Recognition:** Identify dishes from photos taken with your camera or uploaded from your gallery.
*   **Ingredient Identification & Recipe Suggestions:** Get a list of ingredients and tailored recipe ideas for the recognized meal.
*   **Detailed Nutritional Analysis:** View calorie content, macronutrients, and other nutritional data.
*   **Allergen Detection:** Automatically highlights potential allergens (e.g., gluten, dairy, nuts) in the identified meal.
*   **Step-by-Step Cooking Instructions:** Easy-to-follow guides for preparing your dish.
*   **AI Assistant Chatbot:** Get answers to your cooking questions directly within the app.
*   **Save Favorite Recipes:** Build your personal cookbook by saving recipes for later.
*   **Voice Assistance:** Have recipes read aloud to you for a hands-free cooking experience.

### 📱 Mobile & Service Features
*   **Seamless Camera & Gallery Integration**
*   **Text-to-Speech (TTS)** for recipe instructions.
*   **Personalized User Profiles** and meal history logging.
*   **Cloud-based AI Processing** for fast and accurate recognition.

---

## 🛠️ Technology Stack

| Component | Technology / Service |
| :--- | :--- |
| **Mobile Framework** | Flutter (Cross-platform for iOS & Android) |
| **UI/UX Design** | Figma |
| **Core AI Model** | Custom pipeline based on **Recipe1M+** dataset |
| **Computer Vision** | ResNet-50, Vision Transformers (ViT) |
| **Natural Language Processing** | Fine-tuned BERT, Sentence-BERT (SBERT) |
| **Backend API** | Spoonacular API (for recipes & nutrition) |
| **Additional Dataset** | Arabic Food 101 (for local cuisine support) |

---

## 🚀 Getting Started

### Prerequisites
*   Flutter SDK (version 3.0 or above)
*   Dart SDK
*   An IDE like Android Studio or VS Code with the Flutter plugin.
*   A Spoonacular API key ([Get one here](https://spoonacular.com/food-api))

### Installation & Setup

1.  **Clone the repository**
    ```bash
    git clone https://github.com/layanbuirat/Computer-Engineering-2021-2026-Graduation-Intro-19-2-2025-8-7-2025-4.5.git
    cd Computer-Engineering-2021-2026-Graduation-Intro-19-2-2025-8-7-2025-4.5
    ```

2.  **Install Dependencies**
    ```bash
    flutter pub get
    ```

3.  **Configure API Keys**
    *   Create a `.env` file in the root directory based on the provided `.env.example`.
    *   Add your Spoonacular API key:
        ```
        SPOONACULAR_API_KEY=your_api_key_here
        ```

4.  **Run the Application**
    ```bash
    flutter run
    ```

---

## 📸 Screenshots

| Login Screen | Meal Scanning | Recipe Details | AI Assistant |
| :---: | :---: | :---: | :---: |
| <img src="screenshots/login.png" width="150"> | <img src="screenshots/scan.png" width="150"> | <img src="screenshots/recipe.png" width="150"> | <img src="screenshots/assistant.png" width="150"> |

---

## 🏗️ System Architecture

The application follows a client-server architecture:
1.  **Client (Flutter App):** Handles user interaction, camera control, and displays results.
2.  **Server (Python/Flask/Django):** Hosts the pre-trained deep learning model (based on Recipe1M+).
3.  **External API (Spoonacular):** Enriches the results with detailed recipe and nutritional data.

**Workflow:**
1.  User captures/uploads a food image.
2.  Image is sent to the server.
3.  The AI model processes the image and identifies the dish.
4.  The dish name is used to fetch detailed information from the Spoonacular API.
5.  All data (recipe, ingredients, nutrition, allergens) is compiled and sent back to the app for display.

*(Refer to the `system_structure/` directory for detailed diagrams).*

---

## 📁 Project Structure

```
lib/
├── main.dart                 # Application entry point
├── models/                  # Data models (Recipe, User, etc.)
├── views/                   # UI Screens (Login, Scanner, Recipe, etc.)
├── view_models/             # State management (e.g., using Provider/Bloc)
├── services/                # Business logic & API calls (Spoonacular, AI Model)
├── utils/                   # Helpers & constants
└── widgets/                 # Reusable UI components
assets/
├── ai_models/               # TensorFlow Lite models (if used on-device)
└── datasets/                # Links or info for Recipe1M+ & Arabic Food 101
```

---

## 🎯 Project Objectives & Status

| Objective | Target Status | Current Status |
| :--- | :--- | :--- |
| Food Recognition Accuracy | > 85% | In Development 🟡 |
| Image Processing Response Time | < 2 seconds | In Development 🟡 |
| Support for Regional Cuisines | > 50 variations | ✅ (via Datasets) |
| Allergen Detection | Implemented | ✅ (Core Feature) |
| Cross-Platform (iOS/Android) | Implemented | ✅ (via Flutter) |

---

## 🤝 Contributing

We welcome contributions! Please feel free to submit issues, fork the repository, and create pull requests.
1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 👥 Team

This project was developed as a graduation project at **Birzeit University** by:
*   **Rana Musa** ([@RanaMusa](https://github.com/RanaMusa12))
*   **Layan Burait** ([@layanbuirat](https://github.com/layanbuirat))
*   **Haneen Odeh** ([@HaneenOdeh](https://github.com/haneen-odehh))

**Supervised by:** Dr. Yazan Abu Farha

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🔗 Acknowledgments

*   [Recipe1M+ Dataset](https://paperswithcode.com/dataset/recipe1m) for providing the foundational training data.
*   [Spoonacular API](https://spoonacular.com/food-api) for comprehensive recipe and nutritional information.
*   [Arabic Food 101 Dataset](https://www.kaggle.com/datasets/araraltawil/arabic-food-101) for supporting local cuisine.
*   The Flutter and TensorFlow communities for their excellent tools and documentation.

---

