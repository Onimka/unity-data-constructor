<img width="1894" height="550" alt="image" src="https://github.com/user-attachments/assets/89785a8e-8ee7-4911-81ff-847093a13185" />### Предисловие ###
Базовая информация о работе конструктора:
* Конструктор работает на JSON данных: Templates, Data, Localizatins, Logs и так далее.
* Он имеет поддержку сохранения созданных вами данных: локально (Assets/Data Costructor), облачно(на данный момент есть только поддержка Firebase Realtime database).
* Ссылки на ваши юнити ресурсы(картинки, звуки модели и всё что лежит внутри папки проекта) хранятся в системном Scriptable Object, это сделано с целью того чтобы они попали в ваш билд, у вас так же усть возможность менежмента этих ресурсов во вкладке ** Resources **.
** Data ** является списком, экзампляры которого реализуют выбранный ** Template **.
* Вы можете создавать неограниченное кол-во ** Data ** на любой ** Template **.
Поскольку я верду одиночкую разработку, есть много аспектов, которые я не могу проверить или успевать реализовать, мне хотело бы чтобы этот редактор помог разработчикам игр, и мне в том числе, сделать подход к работе с данными более легким.

Installation:
Addressables Installation (required)
Open Window > Package Manager
Switch to Unity Registry view
Find Addressables and click Install

Copy the Plugin folder into your Assets

Инициализация при запуске игры:
Чтобы инициализировать работу редактора в момент запуска вашей игры, вам нужно вызвать: DataConstructor.Initializer.Init();
Там будут списке ваших данных, они будут иметь те же название что вы создавали в Data, и наследоваться от классов которые вы создавали в Template

Первый запуск:
Найди в вернем тул баре Data Constructor, затем нажмите Launch
<img width="903" height="57" alt="image" src="https://github.com/user-attachments/assets/08e17ac6-c2b6-4b7a-b265-bf57a376f808" />
Запустится редактор, он автоматически создаст нужные ему папки
У вас будет несколько вкладок, пока нам нужны только: ** Templates ** и ** Data **

1. Первый Template
Перейдите во вкладку Template
<img width="1900" height="208" alt="image" src="https://github.com/user-attachments/assets/e31d3dd8-f963-47b0-8f83-647fca568cb8" />
1.Найдите Create левой панели (там будут все ваши классы)
<img width="1877" height="862" alt="image" src="https://github.com/user-attachments/assets/3e3fab61-3a76-449e-b27c-d32b72570382" />
2. После нажатия, вам откроется окно в котором вы можете заполнить данные, пока нам хватит только названия
После создания вы можете открыть созданный вами ** Template **
<img width="1918" height="895" alt="image" src="https://github.com/user-attachments/assets/3e8993f3-4643-4ec2-8e46-e9396bd94836" />
1.нажмите ** Add Field **
2.Заполните данные поля, выберите из списка списка тип поля, который вам нужен
Ваш ** Template ** создан.

2. Первый Data
   Перейдите во вкладку Data
   <img width="1892" height="859" alt="image" src="https://github.com/user-attachments/assets/f4d61e40-7936-4e62-9a6a-34222040efbd" />
   1. нажмите Create
   2. Заполните данные (выберите тот Template который вы создали)
   3. Найдите его в левой панели
    <img width="1894" height="550" alt="image" src="https://github.com/user-attachments/assets/7be7f1fb-8a6f-4fef-9938-e696eb0f08da" />
   нажмите ** Add Entry **, создастся экземпляр класа, вы можете его заполнить необходимыми данными.
   После сделанных изменений можете нажать ** Save ** или ** Reset **.

3. Первый Deploy
   Перейдите во вкладку Deploy
   <img width="1897" height="624" alt="image" src="https://github.com/user-attachments/assets/62a30f6c-2b74-4671-bdfd-447246f8e3ff" />

   1. Deploy делает генерацию созданных данных и классов под них.
   2. Нажмите эту кнопку и дожитесь окончания компиляции
   3. После этого у вас в коде появится доступ к вашим данным заполненным данным (пример:  IReadOnlyList<TestTemplate> testData = DataConstructor.DataManager.TestData;)
Вы прошли ознокомительный этап по работе с конструктором, остальную более детальную документацию я напишу в других разделах
