# image_moderation_system

1.Бизнес-анализ (Business Understanding)

Организационная структура: я
Бизнес-цель проекта:
Создание надежного автоматизированного сервиса по обнаружению неподобающих изображений.
Основные задачи:
Улучшение пользовательского опыта за счет выявления и удаления нежелательного контента, что поможет снизить отток пользователей.
Поддержание и укрепление репутации сервиса.
Соблюдение законодательных норм в части обеспечения безопасности контента.
Разработанные решения - существуют, невозможно использовать из-за политик конфиденциальности.

1.1 Текущая ситуация (Assessing current solution)
Доступное железо - 4090 rtx 24 gb, amd ryzen 7950, 64 gb ram - должно быть достаточно для transfer learning и обучения модели с нуля.
Данные будут храниться локально.
Датасеты: NSFW - https://github.com/EBazarov/nsfw_data_source_urls, NSFW_detect - https://huggingface.co/datasets/deepghs/nsfw_detect, Selfie dataset - https://www.crcv.ucf.edu/research/data-sets/selfie/
Вероятные риски - зашумленность данных, не уложиться в сроки.

1.2 Решаемые задачи с точки зрения аналитики (Data Mining goals)

Предварительный выбор метрик:

Accuracy: Общая точность, если классы сбалансированы. Цель: 80-90%

Precision и Recall: Ключевые для оценки ошибок – важно минимизировать как ложные срабатывания (false positives), так и пропуски (false negatives). Цель: 80–90% 

F1-мера: Гармоническое среднее Precision и Recall, обеспечивая баланс между ними. Цель: 80%-90%

AUC (Area Under Curve): Для оценки способности модели различать классы. Цель: 0.8-0.9

1.3 План проекта:

Бизнес-анализ (неделя 1):
Определение целей, требований к модели; анализ существующих решений.

Анализ данных (неделя 2):
Исследование датасетов, оценка объёма, качества и баланса классов.

Подготовка данных (неделя 3):
Предобработка: изменение разрешения, нормализация, аугментация, удаление дубликатов.

Моделирование (неделя 4):
Использование transfer learning с дообучением; при необходимости эксперименты с обучением с нуля.

Оценка результата(неделя 5):
Анализ ошибок и корректировка модели.

Внедрение (неделя 6):
Деплой модели, настройка API и мониторинга, документирование процессов.