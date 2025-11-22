## Предисловие

Базовая информация о работе конструктора:

- Конструктор работает с JSON данными: Templates, Data, Localizations, Logs и другие
- Поддерживает сохранение созданных данных:
  - Локально (Assets/Data Constructor)
  - Облачно (в настоящее время поддерживается только Firebase Realtime Database)
- Ссылки на Unity ресурсы (изображения, звуки, модели и другие ресурсы проекта) хранятся в системном Scriptable Object для включения в билд
- Управление ресурсами доступно во вкладке **Resources**

**Data** представляет собой список экземпляров, реализующих выбранный **Template**
- Вы можете создавать неограниченное количество **Data** для любого **Template**

## Установка

### Установка Addressables (обязательно)

1. Откройте `Window > Package Manager`
2. Переключитесь на представление `Unity Registry`
3. Найдите `Addressables` и нажмите `Install`

### Установка плагина

Скопируйте папку `Plugin` в вашу папку `Assets`

## Инициализация при запуске игры

Для инициализации редактора в момент запуска игры вызовите:

```csharp
DataConstructor.Initializer.Init();
```
Там будут списке ваших данных, они будут иметь те же название что вы создавали в Data, и наследоваться от классов которые вы создавали в Template


## Первый запуск: ##
Найди в вернем тул баре Data Constructor, затем нажмите Launch
<img width="903" height="57" alt="image" src="https://github.com/user-attachments/assets/08e17ac6-c2b6-4b7a-b265-bf57a376f808" />
Запустится редактор, он автоматически создаст нужные ему папки
У вас будет несколько вкладок, пока нам нужны только: **Templates** и **Data**

### 1. Первый Template ###

<img width="1900" height="208" alt="image" src="https://github.com/user-attachments/assets/e31d3dd8-f963-47b0-8f83-647fca568cb8" />
Перейдите во вкладку Template

<img width="1877" height="862" alt="image" src="https://github.com/user-attachments/assets/3e3fab61-3a76-449e-b27c-d32b72570382" />
1.Найдите Create левой панели (там будут все ваши классы)
2. После нажатия, вам откроется окно в котором вы можете заполнить данные, пока нам хватит только названия
После создания вы можете открыть созданный вами **Template**

<img width="1918" height="895" alt="image" src="https://github.com/user-attachments/assets/3e8993f3-4643-4ec2-8e46-e9396bd94836" />
3.нажмите **Add Field**
4.Заполните данные поля, выберите из списка списка тип поля, который вам нужен
Ваш ** Template ** создан.

### 2. Первый Data ###
   Перейдите во вкладку Data
   <img width="1892" height="859" alt="image" src="https://github.com/user-attachments/assets/f4d61e40-7936-4e62-9a6a-34222040efbd" />
   1. нажмите Create
   2. Заполните данные (выберите тот Template который вы создали)
   3. Найдите его в левой панели
    <img width="1894" height="550" alt="image" src="https://github.com/user-attachments/assets/7be7f1fb-8a6f-4fef-9938-e696eb0f08da" />
   нажмите ** Add Entry **, создастся экземпляр класа, вы можете его заполнить необходимыми данными.
   После сделанных изменений можете нажать **Save** или **Reset**.

### 3. Первый Deploy ###
   Перейдите во вкладку Deploy
   <img width="1897" height="624" alt="image" src="https://github.com/user-attachments/assets/62a30f6c-2b74-4671-bdfd-447246f8e3ff" />

   1. Deploy делает генерацию созданных данных и классов под них.
   2. Нажмите эту кнопку и дожитесь окончания компиляции
   3. После этого у вас в коде появится доступ к вашим данным заполненным данным (пример:  IReadOnlyList<TestTemplate> testData = DataConstructor.DataManager.TestData;)
Вы прошли ознокомительный этап по работе с конструктором, остальную более детальную документацию я напишу в других разделах
