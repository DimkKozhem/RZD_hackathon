# RZD_hackathon
## Безопасный маршрут (задача от РЖД, «Цифровой прорыв», 2023, г. Хабаровск)

**Разработчик:** Команда "Деревяшки"

### Описание задачи
При движении моторвагонного подвижного состава имеют место случаи выхода на маршрут следования людей, попадания посторонних предметов на железнодорожные пути или выезд автотранспорта. В таких ситуациях без преувеличения важна каждая секунда, и, если локомотивная бригада не принимает оперативных мер по причине отвлечения от контроля маршрута следования, может произойти трагедия. Аналогичные требования относятся и ко времени реагирования на случаи следования на «красный» сигнал светофора. Своевременное реагирование в данных ситуациях - это спасённые жизни и предотвращение случаев нарушения безопасности движения. 

### Задача участников
Участникам хакатона предстоит создать систему контроля за состоянием пути, показанием светофоров (готовность маршрута), наличия посторонних лиц, предметов на железнодорожном полотне, препятствующих свободному следованию подвижного состава, приближающихся транспортных средств. Система должна анализировать видеопоток постоянно и при выявлении людей или посторонних предметов, запрещающего «красного» сигнала светофора иметь возможность послать сигнал на устройство световой и звуковой индикации.

### Подходы к решению задачи

#### Подход 1: Классификация
- Разбиение видео на кадры
- Ручная разметка
- Обучение классификатора

Запустить проект по первому подходу можно по [ссылке](https://colab.research.google.com/drive/11ooC0uXf1_rgXTmYHThdsqpOs1uUFwu7?usp=sharing).

**Веса модели после обучения в файле:** `efficient_weights.pth`

**Ноутбук с решением:** `RZD_hack.ipynb`

Используемые библиотеки:
- ultralytics
- opencv-python
- pandas
- numpy
- Pytorch
- openCV
- torchmetrics

#### Подход 2: Детекция
- Поиск объектов при помощи YOLO8 в определенных областях видеопотока

**Ноутбук с решением:** `baseline_yolo8_v2.ipynb`

**Файл модели:** `model_v1.py`

Используемые библиотеки:
- ultralytics
- opencv-python
- pandas
- numpy

### Использованные данные
В работе использовались обезличенные данные от РЖД:
- `train_dataset_Безопасный маршрут`

### Контакты
Для связи с нами обращайтесь к [Dimk_88](https://t.me/Dimk_88).
