# Open-Source RAG Q&A система

Полноценная локальная RAG (Retrieval-Augmented Generation) система для вопросно-ответной работы с документами, построенная на 5 открытых инструментах.

## Особенности
- **Ингestion документов**: Конвертация PDF в markdown с помощью Microsoft MarkItDown
- **Интеллектуальное разделение текста**: Разбивка на чанки с помощью LangChain
- **Семантический поиск**: Эмбеддинги SentenceTransformers + векторная база ChromaDB
- **Локальная LLM**: Интеграция с Ollama (Llama 3.2) для генерации ответов
- **Веб-интерфейс**: Gradio с потоковой выдачей ответов и указанием источников

## Быстрый старт

1. Установите зависимости:
```bash
pip install markitdown[pdf] sentence-transformers langchain-text-splitters chromadb gradio langchain-ollama
curl -fsSL https://ollama.com/install.sh | sh
ollama pull llama3.2
```

2. Загрузите руководство по Python (Think Python) или используйте собственный PDF.

3. Запустите Jupyter notebook для:
   - Конвертации документов
   - Создания векторной базы данных
   - Запуска интерактивного Q&A интерфейса

## Технологии
- **MarkItDown** – Конвертация PDF в markdown
- **SentenceTransformers** – Локальные эмбеддинги (multi-qa-mpnet-base-dot-v1)
- **LangChain** – Разделение текста и оркестрация LLM
- **ChromaDB** – Векторное хранилище
- **Gradio** – Веб-интерфейс с потоковой выдачей
- **Ollama** – Локальные LLM

## Структура проекта
```
├── documents/          # Исходные PDF-файлы
├── processed_docs/     # Конвертированные markdown-файлы
├── chroma_db/         # Векторная база данных
└── notebook.ipynb     # Полный пайплайн системы
```

## Пример использования
Задавайте вопросы о программировании на Python (или по вашим документам) и получайте точные ответы с примерами кода и указанием источников.

Вся обработка происходит локально — без API-ключей и облачных сервисов.
