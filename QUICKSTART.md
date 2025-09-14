# 🚀 Быстрый старт - Dialogs RAG System v2.0

## Установка и запуск за 5 минут

### 1. Установка зависимостей
```bash
python setup.py
```

### 2. Настройка API ключа
Отредактируйте файл `.env` и добавьте ваш OpenAI API ключ:
```bash
OPENAI_API_KEY=your_api_key_here
```

### 3. Тестирование системы
```bash
# Тест без OpenAI (быстрый)
python test_system.py

# Тест с примером данных
make example-data
python main.py --input data/input/dialogs.xlsx --dry-run --verbose
```

### 4. Обработка ваших данных
```bash
# Поместите ваши файлы в data/input/
python main.py --input data/input/your_dialogs.xlsx --verbose
```

## 📁 Структура проекта

```
dialogs-rag-v2/
├── src/                    # Исходный код
│   ├── config/            # Конфигурация
│   └── pipeline/          # Модули обработки
├── data/                  # Данные
│   ├── input/             # Входные файлы
│   └── output/            # Результаты
├── logs/                  # Логи
├── tests/                 # Тесты
├── main.py               # Главный файл
├── setup.py              # Установка
└── test_system.py        # Тестирование
```

## 🔧 Основные команды

```bash
# Установка
python setup.py

# Тестирование
python test_system.py

# Обработка данных
python main.py --input data/input/dialogs.xlsx

# Создание примера данных
make example-data

# Пробный запуск
python main.py --input data/input/dialogs.xlsx --dry-run
```

## 📊 Что делает система

1. **Загружает диалоги** из Excel/CSV/JSON файлов
2. **Извлекает сущности** с помощью OpenAI GPT:
   - Проблемы и барьеры
   - Идеи и предложения
   - Упоминания доставки
   - Сигналы и индикаторы
3. **Создает эмбеддинги** для семантического анализа
4. **Кластеризует** похожие сущности
5. **Генерирует отчеты** с анализом

## 🎯 Результаты

Система создает в папке `data/output/`:
- Обработанные диалоги с извлеченными сущностями
- Эмбеддинги для семантического поиска
- Кластеры похожих сущностей
- Детальные отчеты в JSON формате

## 🆘 Помощь

- **Проблемы с установкой**: Запустите `python setup.py`
- **Ошибки API**: Проверьте `.env` файл
- **Медленная работа**: Уменьшите `batch_size` в `config.yaml`
- **Логи**: Смотрите в папке `logs/`

## 📞 Поддержка

При возникновении проблем:
1. Запустите `python test_system.py`
2. Проверьте логи в `logs/`
3. Создайте Issue в репозитории
