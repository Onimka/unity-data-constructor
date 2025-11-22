## Preface

Basic information about the Data Constructor:

- The constructor works with JSON data: Templates, Data, Localizations, Logs, and more.
- Supports saving created data:
  - Locally (Assets/Data Constructor)
  - Cloud (currently only Firebase Realtime Database is supported)
- References to Unity assets (images, sounds, models, and other project resources) are stored in a system Scriptable Object for inclusion in the build.
- Asset management is available in the **Resources** tab.

**Data** represents a list of instances based on a chosen **Template**.  
- You can create an unlimited number of **Data** instances for any **Template**.

## Installation

### Addressables Installation (required)

1. Open `Window > Package Manager`.
2. Switch to the `Unity Registry` view.
3. Find `Addressables` and click `Install`.

### Plugin Installation

Copy the `Plugin` folder into your `Assets` folder.

## Initialization on Game Start

To initialize the editor at runtime, call:

```csharp
DataConstructor.Initializer.Init();
```
Your data lists will appear there, using the same names you created in `Data`, and they will inherit from the classes defined in your `Templates`.

## First Launch

Find `Data Constructor` in the top toolbar and click `Launch`:  
<img width="903" height="57" alt="image" src="https://github.com/user-attachments/assets/08e17ac6-c2b6-4b7a-b265-bf57a376f808" />

The editor will start and automatically create the required folders.  
You will see several tabs; for now, we only need: `Templates` and `Data`.

### 1. Creating the First Template
<img width="1900" height="208" alt="image" src="https://github.com/user-attachments/assets/e31d3dd8-f963-47b0-8f83-647fca568cb8" />

Go to the `Templates` tab:  
<img width="1877" height="862" alt="image" src="https://github.com/user-attachments/assets/3e3fab61-3a76-449e-b27c-d32b72570382" />

1. Find `Create` on the left panel (this contains all your classes).  
2. Click it, and a window will open where you can fill in the data (for now, only the name is required).  
3. After creation, open the `Template` you just created:  
<img width="1918" height="895" alt="image" src="https://github.com/user-attachments/assets/3e8993f3-4643-4ec2-8e46-e9396bd94836" />

4. Click `Add Field`.  
5. Fill in the field data and select the desired field type from the list.

Your **Template** is now created.

### 2. Creating the First Data
Go to the `Data` tab:  
<img width="1892" height="859" alt="image" src="https://github.com/user-attachments/assets/f4d61e40-7936-4e62-9a6a-34222040efbd" />

1. Click `Create`.  
2. Fill in the data (select the Template you created).  
3. Find it in the left panel:  
<img width="1894" height="550" alt="image" src="https://github.com/user-attachments/assets/7be7f1fb-8a6f-4fef-9938-e696eb0f08da" />

4. Click `Add Entry` to create a class instance, which you can then fill with the required data.  
5. After making changes, click `Save` or `Reset`.

### 3. First Deploy
Go to the `Deploy` tab:  
<img width="1897" height="624" alt="image" src="https://github.com/user-attachments/assets/62a30f6c-2b74-4671-bdfd-447246f8e3ff" />

1. `Deploy` generates classes and data from your created entries.  
2. Click the button and wait until compilation finishes.  
3. After that, your data becomes accessible in code (example:  
```csharp
IReadOnlyList<TestTemplate> testData = DataConstructor.DataManager.TestData;
```
      
You have passed the chilling stage of working with the constructor, I will write the rest of the more detailed documentation in other sections.
