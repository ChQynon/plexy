# Модели искусственного интеллекта в Plexy

Plexy использует различные модели Google Gemini AI для обработки запросов пользователей. Каждая модель имеет свои особенности и предназначение.

## Доступные модели

### Стандартная модель (gemini-2.5-pro-exp-03-25)

**Описание:** Универсальная модель Gemini с высокой производительностью для общего назначения. Эта модель хорошо справляется с большинством задач, включая ответы на вопросы, генерацию текста, объяснения и т.д.

**Характеристики:**
- Temperature: 1.0
- Top-P: 0.95
- Top-K: 64
- Максимальное количество токенов: 65536
- Подходит для: общих вопросов, создания контента, объяснений, переводов

### Модель с рассуждениями (gemini-2.0-flash-thinking-exp-01-21)

**Описание:** Эта модель специализируется на задачах, требующих углубленного анализа и рассуждений. Она демонстрирует свой "ход мыслей", что помогает пользователям понять, как она пришла к определенному выводу.

**Характеристики:**
- Temperature: 0.7 (более консервативная для точных рассуждений)
- Top-P: 0.95
- Top-K: 64
- Максимальное количество токенов: 65536
- Подходит для: решения задач, логических головоломок, анализа данных, обучения

### Генератор изображений (gemini-2.0-flash-exp-image-generation)

**Описание:** Модель, специализирующаяся на работе с изображениями. Может как анализировать и описывать изображения, так и генерировать их по текстовому описанию.

**Характеристики:**
- Temperature: 1.0
- Top-P: 0.95
- Top-K: 40
- Максимальное количество токенов: 8192
- Модальности ответа: изображения и текст
- Подходит для: анализа изображений, создания изображений, работы со стикерами

## Когда использовать какую модель

- **Стандартная модель** — подходит для большинства повседневных запросов, общих вопросов и генерации текста.
- **Модель с рассуждениями** — лучше использовать, когда вам нужно понять процесс мышления ИИ или решить сложные задачи.
- **Генератор изображений** — автоматически используется при отправке фотографий или когда вы хотите получить визуальный ответ.

## Переключение между моделями

Для смены модели используйте команду `/setmodel` с номером модели:

```
/setmodel 1 - Выбрать генератор изображений
/setmodel 2 - Выбрать стандартную модель
/setmodel 3 - Выбрать модель с рассуждениями
```

Для просмотра списка всех доступных моделей используйте команду `/models`.

## Особенности работы с моделями

- При смене модели история чата сбрасывается, так как разные модели имеют разные контексты и способы обработки запросов.
- Если вы отправляете изображение, Plexy автоматически переключится на модель для работы с изображениями, даже если выбрана другая модель.
- Каждая модель имеет свой стиль ответов и поведение, что позволяет выбрать наиболее подходящую для конкретной задачи. 