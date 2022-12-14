# Module28_Evaluation
финальный нотбук по задаче предсказания стоимости поддержанного автомобиля

Постановка общей задачи: работаем с небольшой выборкой из коллекции подержанных автомобилей, 
выставленных на продажу в Соединённых Штатах. На этих данных вам нужно построить модель классификации, 
определяющую категорию цены подержанного автомобиля в зависимости от характеристик транспортного средства. Описание датасета: 
id: идентификатор записи;url: URL записи о продаже;region: регион;region_url: URL региона;price: стоимость;year: год выпуска;manufacturer: производитель;model: модель;condition: состояние;cylinders: количество цилиндров;fuel: тип топлива;odometer: количество пройденных миль;title_status: статус;transmission: коробка передач;VIN: идентификационный номер;drive: тип привода;size: размер;type: кузов;paint_color: цвет;image_url: URL изображения;description: указанное описание;county: страна;state: штат;lat: широта;long: долгота;posting_date: дата размещения объявления о продаже;price_category: категория цены.
 
Data Preparation:
произведится преобразование типов данных, если нужно; исследуем данные на пропуски, обработываем их (например, заполните какими-то значениями);
избавляемся от аномалий.

Feature engineering:
Объявите блок Feature engineering. В этом блоке:
готовим  категориальные переменные с помощью OneHotEncoder;стандартизируем и нормализуем переменные;создайте новые признаки на основе информации в датафрейме 
(на основе дат, текстовых значений переменных, и так далее); удаляем неинформативные колонки, которые появились в датасете в результате Feature engineering;
сформируем финальный датасет, на котором будет производиться моделирование, и сохраняем его в отдельный файл.

Modelling:
сформируем датасет для обучения; инициализируем фичи и целевую переменную 
(price_category); 
положм их в соответствующие переменные;
разделм данные на треин и тест;объявляем три модели: логистическая регрессия, случайный лес и многослойный персептрон;
делаем тюнинг параметров и выбераем лучшую модель с помощью кросс-валидации на тренировочной выборке;
по результатам кросс-валидации выбераем лучшую модель;
считаем  значение метрики лучшей модели на тестовой выборке;

Results:
Объявите блок Results. В этом блоке:
подведим итог: какая модель показала себя лучше всего и будет финальным результатом данного ноутбука;
обучаем эту модель на всём датасете;
сохраняем обученную модель в pickle.
