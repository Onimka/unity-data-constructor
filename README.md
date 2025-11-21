🧩 Unity Data Constructor 🚧

Unity Data Constructor is a powerful and flexible Unity Editor extension for visually constructing and managing structured game data.
It’s designed to simplify and accelerate your configuration workflow — ideal for both designers and developers.

⚠️ Currently in active development. UI, UX, and features may change.

✨ Features

🧩 Template-based system for reusable data structures
📋 List support with reorder and inline editing
🧬 Full support for nested fields and complex types
🧠 Works with abstract classes and inheritance hierarchies
🧱 Supports all UnityEngine.Object-based types (e.g., Prefab, ScriptableObject, Texture, AudioClip)
🔗 External field references across templates
💾 Import/export with clean JSON serialization
🖱️ Clean, scalable, and intuitive UI
🧪 Seamless Unity Editor integration

Install Addressables Package (Required Dependency):
1. Open Window > Package Manager
2. Switch to Unity Registry view
3. Find Addressables and click Install

Install Data Constructor:
1. Copy Plugin folder in Assets
2. Runtime initialize - DataConstructor.Initializer.Init();
3. Your Datas located in runtime DataConstrucrtor.DataManager.YOUR_DATA_NAME (Example: List<DataConstrucrtor.DataManager.ExampleClass> ExampleData)


⚙️ Requirements:
Unity 2021.3+ (LTS recommended)
Addressables Package 1.21.0+
.NET 4.x Runtime

Team Development.
Support Firebase Realtime Database for cloude database.

📸 Preview
<img width="1919" height="1025" alt="image" src="https://github.com/user-attachments/assets/4677d1e1-ee3d-4143-8644-70c8b18b1fe4" /> <img width="1919" height="1012" alt="image" src="https://github.com/user-attachments/assets/56b56375-7af8-4b87-885d-3c294822d966" />
🛠️ How It Works

Define your data structures using serializable C# classes (including abstract bases or inherited types).

<img width="1899" height="958" alt="image" src="https://github.com/user-attachments/assets/6d42cd43-e709-4542-a3ae-b43a96cf90ac" />

Use the editor to add fields, including nested structures or Unity object references.

Create data files and entries visually.

<img width="1919" height="982" alt="image" src="https://github.com/user-attachments/assets/f04e02b6-1077-41b8-9fdf-b43e9c898d06" />

Auto-generate C# code and final JSON data files.

At runtime, your game automatically loads parsed JSON data from the generated file.

Localization.
<img width="2560" height="1020" alt="image" src="https://github.com/user-attachments/assets/72060d0e-6d82-4555-a207-f7e0dc124048" />
Support localized string. Auto-translate with support local ollama and other services.

Resources.
<img width="2559" height="1033" alt="image" src="https://github.com/user-attachments/assets/c13cf51e-7bc1-44c5-9ae4-73b5fb37a4bd" />


❓ Troubleshooting
Addressables Not Found?

Ensure you're using Unity 2021.3+

Check Package Manager shows Addressables as "Installed"

Restart Unity if issues persist

Import Errors?

Verify internet connection for Git URL installation

Check Unity Console for specific error messages

Ensure .NET 4.x Runtime is selected in Player Settings

🚧 Roadmap

🔍 Search and filtering
✅ Field validation & constraints
🌍 Localization-ready fields
🧰 Preset templates & plugin architecture
🎯 Drag-and-drop Unity assets

🧑‍💻 License

This tool is free to use in personal and commercial Unity projects.
However, modification, redistribution, or republishing of the source code is not allowed.

© 2025 Onimka. All rights reserved.
