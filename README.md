# 🤖 ML Model - Real-time Image Classification Android App


A modern Android application that performs **real-time image classification** using TensorFlow Lite and MobileNet v1. Built with Jetpack Compose for a minimal, native Android experience.

## ✨ Features

- **🎯 Real-time Classification** - Instant object recognition through camera feed
- **📱 Minimal UI** - Clean interface built entirely with Jetpack Compose
- **🧠 TensorFlow Lite Integration** - Optimized MobileNet v1 model for mobile devices
- **📸 Camera Integration** - Seamless CameraX implementation
- **🎨 Material 3 Design** - Contemporary Android design language
- **⚡ High Performance** - Efficient image processing and prediction

## 🚀 Getting Started

### Prerequisites

- Android Studio Arctic Fox or later
- Android SDK 21+
- Physical Android device (recommended for camera functionality)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ml-model-android.git
   cd ml-model-android
   ```

2. **Add model files**
   
   Place these files in `app/src/main/assets/`:
   - `mobilenet_v1_1.0_224_quant.tflite` - The quantized MobileNet model
   - `labels.txt` - ImageNet class labels

3. **Build and run**
   
   Open the project in Android Studio and run on your device.

## 📱 How It Works

The app uses a sophisticated pipeline to deliver real-time classification:

1. **Camera Feed** - CameraX captures live video frames
2. **Image Processing** - Frames are resized to 224x224 pixels
3. **Model Inference** - TensorFlow Lite runs MobileNet v1 predictions
4. **Results Display** - Top predictions shown with confidence scores

## 🏗️ Architecture

```
📦 com.humblecoders.mlmodel
 ┣ 📂 ui/theme/
 ┃ ┣ 📜 Color.kt         # Material 3 color scheme
 ┃ ┣ 📜 Theme.kt         # App theming configuration
 ┃ ┗ 📜 Type.kt          # Typography definitions
 ┗ 📜 MainActivity.kt    # Main app logic & ML inference
```

### Key Components

- **`MainActivity`** - Entry point with camera permission handling
- **`ImageClassifierApp`** - Main Compose UI with live classification
- **`ImageClassifier`** - TensorFlow Lite model wrapper and inference logic
- **`startCamera`** - CameraX setup and image analysis pipeline

## 🛠️ Technical Stack

- **Language**: Kotlin
- **UI Framework**: Jetpack Compose
- **Camera**: CameraX
- **ML Framework**: TensorFlow Lite
- **Model**: MobileNet v1 (224x224, Quantized)
- **Design System**: Material 3

## 📊 Model Details

- **Architecture**: MobileNet v1
- **Input Size**: 224 × 224 × 3
- **Quantization**: 8-bit integer
- **Classes**: 1,000 ImageNet categories
- **Size**: ~4.3 MB

## 🎯 Performance

- **Inference Time**: ~50-100ms on modern devices
- **Memory Usage**: <50MB RAM
- **Confidence Threshold**: 20% (adjustable)

## 🔧 Customization

### Adding New Models

1. Replace the `.tflite` file in assets
2. Update `labels.txt` with new class names
3. Modify input preprocessing in `ImageClassifier.classify()`

### UI Theming

Customize colors in `ui/theme/Color.kt`:
```kotlin
val Purple80 = Color(0xFFD0BCFF)  // Primary color
val PurpleGrey80 = Color(0xFFCCC2DC)  // Secondary color
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📞 Support

If you have any questions or run into issues, please open an issue on GitHub.

---

<div align="center">
  <p>Made with ❤️ by Humble Coders</p>
  <p>⭐ Star this repo if you found it helpful!</p>
</div>
