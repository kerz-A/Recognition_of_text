# Recognition_of_text
Распознавание текста на изображении с использованием нейросетевых методов
# Описание проекта

    Проект направлен на разработку и улучшение моделей для распознавания текста на изображениях, 
    включая детектирование текстовых областей и интерпретацию их содержимого. В рамках проекта были исследованы 
    современные подходы, такие как интеграция моделей YOLO и Faster R-CNN с EasyOCR, для повышения точности распознавания текста.

# Цели проекта

    Создать модель для детектирования текстовых областей и их распознавания.
    Улучшить метрики точности и качества распознавания текста.
    Провести сравнительный анализ подходов с использованием современных нейросетевых методов.

# Используемые данные

    Датасет: ICDAR 2015
        Изображения с текстом, сделанные в реальных условиях.
        Включает текстовые области, размеченные как bounding boxes, и аннотации текста.
        Примеры включают разнообразные фоны, углы наклона текста и нестандартные шрифты.

# Гипотезы

    Нулевая гипотеза (H₀):
        Использование моделей YOLO и Faster R-CNN для улучшения EasyOCR не приводит к значительному улучшению точности 
        распознавания текста.

    Альтернативная гипотеза (H₁):
        Интеграция моделей YOLO и Faster R-CNN с EasyOCR значительно улучшает точность детектирования и распознавания текста.

# Метрики оценки

    Для детектирования:
        IoU (Intersection over Union): качество совпадения предсказанных и истинных bounding boxes.
        Precision, Recall, F1-score: оценка точности нахождения текста.

    Для распознавания текста:
        CER (Character Error Rate): процент ошибок на уровне символов.
        WER (Word Error Rate): процент ошибок на уровне слов.

# Методы и подходы

    Бейзлайн:
        EasyOCR: базовая модель для распознавания текста.

    Улучшенные модели:
        YOLO + EasyOCR: улучшение детектирования bounding boxes.
        Faster R-CNN + EasyOCR: интеграция более точной модели детектирования.

    Техники оптимизации:
        Ограничение размеров bounding boxes.
        Настройка Confidence Threshold для максимизации F1-Score.

# Результаты
        Сравнение моделей
        Метрика 	     EasyOCR 	    YOLO + EasyOCR 	     Faster R-CNN + EasyOCR
        CER 	     80.04% 	    77.87% 	             36.15%
        WER 	     97.25% 	    92.73% 	             69.07%
        IoU 	      4.10% 	     2.32% 	             60.24%
# Основные выводы

    Faster R-CNN + EasyOCR показал наилучшие результаты по метрикам CER и WER.
    YOLO + EasyOCR улучшил точность символов по сравнению с базовой моделью.
    Метрика IoU остаётся низкой, что указывает на необходимость дальнейшей оптимизации детектирования текстовых областей.

# Используемые библиотеки

    pandas
    numpy
    matplotlib
    seaborn
    torch
    transformers
    EasyOCR
    YOLOv5
    Faster R-CNN

# Навыки, продемонстрированные в проекте

    Работа с современными архитектурами компьютерного зрения (YOLO, Faster R-CNN).
    Интеграция OCR-систем с моделями детектирования текста.
    Использование метрик (IoU, CER, WER) для оценки качества моделей.
    Анализ и визуализация результатов экспериментов.

# Возможные улучшения

    Оптимизация моделей детектирования текста для повышения IoU.
    Расширение тренировочного набора данных для улучшения генерализации.
    Сравнение с другими архитектурами, такими как Swin Transformer или CLIP.
