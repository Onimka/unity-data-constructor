# Unity Data Constructor

**Unity Data Constructor** is a powerful and flexible Unity Editor extension for visually creating and managing structured game data.
It is designed to simplify and speed up the configuration workflow — perfect for both designers and developers.

⚠️ Currently in active development. UI, UX, and functionality may change.

## 📖 Guide

Full documentation and usage instructions are available in the [**GUIDE**](https://github.com/Onimka/unity-data-constructor/blob/main/Documentation/README.md)

## ✨ Features

* Template-based system for reusable data structures
* List support with reordering and inline editing
* Full support for nested fields and complex types
* Works with abstract classes and inheritance hierarchies
* Supports all UnityEngine.Object-based types (e.g., Prefab, ScriptableObject, Texture, AudioClip)
* External field references between templates
* Import/export via clean JSON serialization
* Clean, scalable, intuitive interface
* Seamless Unity Editor integration
* Team-friendly: supports Firebase Realtime Database as a cloud storage backend

## 📦 Addressables Installation (required)

1. Open **Window > Package Manager**
2. Switch to **Unity Registry** view
3. Find **Addressables** and click **Install**

## 📥 Installing Data Constructor

1. Copy the **Plugin** folder into your **Assets**
2. Initialize at runtime: `DataConstructor.Initializer.Init();`
3. Access your runtime data via `DataConstructor.DataManager.YOUR_DATA_NAME`

   * Example: `List<DataConstructor.DataManager.ExampleClass> ExampleData`

## ⚙️ Requirements

* Unity 2021.3+ (LTS recommended)
* Addressables 1.21.0+

## 🖼️ Preview

(Images not embedded in this document)

## 🔧 How It Works

1. Define your data structures with serializable C# classes (including abstract or inherited types).
2. Use the editor to add fields, including nested structures or Unity object references.
3. Create data files and entries visually.
4. Automatically generate C# code and final JSON data files.
5. At runtime, the game loads parsed JSON data from the generated file.

## 🌐 Localization

Supports localized strings. Includes automatic translation using local Ollama or external services.

## 📁 Resources

Manage assets used by the constructor directly through the interface.

## 🚧 Roadmap

* Search and filtering
* Field validation and constraints
* Localization improvements
* Settings templates and plugin architecture
* Drag-and-drop of Addressables into the editor window

## 🧑‍💻 License

This tool is free to use in personal and commercial Unity projects.
However, modifying, redistributing, or republishing the source code is not allowed.

© 2025 Onimka. All rights reserved.
