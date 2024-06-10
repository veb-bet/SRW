# Разработка модели глубокого обучения для обнаружения дипфейков

## 1 Введение
### 1.1 Наименование программы
Разрабатываемое приложение предназначено для распознавания дипфейков на видео. Полное наименование программного продукта - "Приложение с методом распознавания подделок с заменой лиц 'Deep Fake'". Далее используется краткое название - "программа".

## 2 Основания для разработки
Разработка ведется на основании задания на выполнение выпускной квалификационной работы бакалавра.

## 3 Назначение разработки
Назначение разработки состоит в создании системы для обнаружения дипфейка в видео. Дипфейк - это видео или изображение, измененное или созданное с помощью искусственного интеллекта для создания ложной информации или обмана. Целью данной разработки является предоставление пользователям инструмента, который поможет обнаружить дипфейк и определить достоверность представленного видео материала. Система будет использовать алгоритмы машинного обучения и компьютерного зрения для анализа видео и определения наличия дипфейка. Результаты анализа будут предоставлены пользователям в удобном формате, а также будут сохранены в истории для их последующего просмотра.

## 4 Требования к программе
### 4.1 Требования к функциональным характеристикам
#### 4.1.1 Требования к составу выполняемых функций
Главной функцией программы должна быть распознавание дипфейков на видео. Программа должна обеспечивать возможность загрузки видео для анализа, поддержку различных форматов видео, распознавание дипфейка в видео, отображение результатов анализа, авторизацию/регистрацию пользователей и сохранение истории. Модель распознавания должна иметь точность больше 60% и скорость распознавания около 10 кадров в секунду.

#### 4.1.2 Требования к организации входных данных
Входными данными программы должны быть логин и пароль пользователя, а также видеофайлы, загруженные с устройства, и их метаданные.

#### 4.1.3 Требования к организации выходных данных
Выходными данными программы должна быть информация о том, является ли видео дипфейком (заголовок видео, длительность, дата загрузки и результат распознавания, вероятность того, что видео является дипфейком), а также персональные данные пользователя (электронная почта или измененная информация профиля).

### 4.2 Требования к надежности
#### 4.2.1 Требования к обеспечению надежного функционирования
Надежное (устойчивое) функционирование программы должно быть обеспечено организацией бесперебойного питания технических средств и использованием лицензионного программного обеспечения.

#### 4.2.2 Время восстановления после отказа
Время восстановления после отказа, вызванного сбоем электропитания технических средств (иными внешними факторами), не фатальным сбоем операционной системы, не должно превышать нескольких минут при условии соблюдения условий эксплуатации технических и программных средств.

#### 4.2.3 Отказы из-за некорректных действий оператора
Отказы программы из-за некорректных действий оператора (пользователя) должны быть исключены или сведены к минимуму за счет использования понятного и интуитивно-понятного интерфейса, а также наличия подробной документации и руководства пользователя.

### 4.3 Условия эксплуатации
#### 4.3.1 Требования к численности и квалификации персонала
Минимальное количество персонала, требуемого для работы программы должно составлять – один пользователь программы.

### 4.4 Требования к составу и параметрам технических средств
Минимальные требования к параметрам технических средств компьютера:
- процессор 2 ГГц;
- операционная система Windows XP;
- память 2 ГБ ОЗУ;
- жёсткий диск 1 ГБ.

### 4.5 Требования к информационной и программной совместимости
#### 4.5.1 Требования к методам решения
Данные методы решения должны обеспечивать выполнение всех этапов проектирования программы в соответствии с их порядком и сроками выполнения, указанными в разделе 6 данного документа.

#### 4.5.2 Требования к исходным кодам и языкам программирования
Исходные коды приложения должны быть реализованы на языке программирования Python. В качестве используемых библиотек:
- os: для работы с операционной системой, в данном случае используется для работы с файловой системой.
- cv2: OpenCV - библиотека компьютерного зрения, используется для работы с изображениями и видео.
- numpy: библиотека для работы с многомерными массивами и математическими операциями.
- sklearn.model_selection: модуль scikit-learn для разделения данных на обучающую и тестовую выборки.
- tensorflow.keras.models: подмодуль Keras библиотеки TensorFlow для создания и обучения моделей глубокого обучения.
- tensorflow.keras.layers: подмодуль Keras библиотеки TensorFlow для создания слоев нейронных сетей. В данном случае используются сверточные и полносвязные слои, а также слой для снижения размерности.
- tensorflow.keras.optimizers: подмодуль Keras библиотеки TensorFlow для оптимизаторов, используемых в процессе обучения модели. В данном случае используется оптимизатор Adam.
- tensorflow.keras.losses: подмодуль Keras библиотеки TensorFlow для функции потерь, используемой в процессе обучения модели. В данном случае используется функция потерь категориальной кросс-энтропии.
- tensorflow.keras.metrics: подмодуль Keras библиотеки TensorFlow для метрик, используемых для оценки производительности модели в процессе обучения. В данном случае используется метрика точности.
- tensorflow.keras.preprocessing.image: подмодуль Keras библиотеки TensorFlow для предварительной обработки изображений. В данном случае используется функция для масштабирования и изменения размера изображений.
- PyQt5.QtWidgets: подмодуль PyQt5 для создания графического интерфейса пользователя (GUI). В данном случае используется для создания окон и виджетов.

Данные версии библиотек обеспечивают необходимую функциональность для реализации приложения. Более новые версии библиотек также могут быть использованы, но необходимо провести дополнительное тестирование, чтобы убедиться в совместимости.

### 4.6 Требования к программным средствам, используемым программой
В состав общесистемного и прикладного программного обеспечения входят операционная система (Microsoft Windows 10 Корпоративная / Microsoft Windows 10 Профессиональная / Microsoft Windows 10 Домашняя расширенная / Microsoft Windows XP).

В качестве интегрированной среды разработки программы должна быть использована среда PyCharm. Также может быть использована среда разработки Google Colab.
Системные программные средства, используемые программой, должны быть представлены лицензионными локализованными версиями программных систем.

## 5 Требования к программной документации
### 5.1 Состав программной документации

Состав программной документации должен включать в себя техническое задание на разработку и проектирование программы (ГОСТ 19), пояснительную записку и исходные коды программы.

## 6 Стадии и этапы разработки
Проектирование программы должно включать следующие стадии:

1. Анализ требований пользователя (Ноябрь 10, 2023 - Ноябрь 27, 2024).
2. Разработка технического задания (Декабрь 1, 2023 - Декабрь 9, 2024).
3. Определение целей и задач проекта (Декабрь 10, 2023 - Январь 9, 2024).
4. Создание обучающей выборки данных для модели (Февраль 2, 2024 - Март 10, 2024).
5. Разработка и обучение модели для распознавания поделок (Март 5, 2024 - Март 15, 2024).
6. Тестирование и оценка эффективности метода распознавания (Март 15, 2024 - Март 20, 2024).
7. Разработка приложения (Март 20, 2024 - Апрель 20, 2024).
8. Тестирование приложения (Апрель 25, 2024 - Май 1, 2024).

В рамках данного проекта внедрение программного продукта не предусмотрено.

## Приложения
<details>
<summary>Диаграммы и схемы</summary>
   
### Диаграммы бизнес-процессов системы распознавания:
![444](https://github.com/veb-bet/Deepfake_recognition_method_in_video/assets/73333734/c4c46078-f08c-4626-a572-786a211e10a7)
![333](https://github.com/veb-bet/Deepfake_recognition_method_in_video/assets/73333734/ae60e632-e9db-472d-bb09-51acac239efa)

### Диаграмма классов:
![1](https://github.com/veb-bet/Deepfake_recognition_method_in_video/assets/73333734/b0788a74-873f-45c4-9006-7c96b2f95b7c)

### Струкрута базы данных:
![2](https://github.com/veb-bet/Deepfake_recognition_method_in_video/assets/73333734/eede3e94-4528-42f4-afd9-c4af26764bd8)

### Структурная схема
![Рисунок1](https://github.com/veb-bet/Deepfake_recognition_method_in_video/assets/73333734/8031e7d8-8cc5-43e8-a715-2382c6e9a004)

</details>

<details>
<summary>Работа приложения</summary>


https://github.com/veb-bet/Deepfake_recognition_method_in_video/assets/73333734/43510ffa-3c8b-4e28-a192-b21fd3464749


   
</details>