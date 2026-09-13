# Бхагавад-гита — Bhagavad Gita

Коллекция источников для изучения Бхагавад-гиты.

## Основной текст

Бхагавад-гита — диалог Кришны и Арджуны, состоящий из 18 глав и 700 стихов (в некоторых традициях счёт отличается на один стих).

### Русский текст онлайн

- [Бхагавад-гита в русских переводах](https://bhagavadgita.ru/) — главы 1–18, несколько русских переводов.
- [Полный текст перевода Б. Л. Смирнова](https://scriptures.ru/bh_gita.htm) — отдельная страница с полным текстом и PDF.
- [Викитека: сведения и библиография по Бхагавад-гите](https://ru.wikisource.org/wiki/НЭС/Багавад-Гита)

### Русский PDF

- [Bhagavad Gita на русском — International Gita Society](https://www.gita-society.com/wp-content/uploads/2019/01/BhagavadGitainRussianLanguage.pdf)

> Важно: русские переводы разных авторов имеют отдельный авторско-правовой статус. В этот репозиторий не копируется целиком современный защищённый перевод без проверки лицензии.

## Оригинал на санскрите

- [Sanskrit Wikisource — Bhagavad Gita](https://sa.wikisource.org/wiki/भगवद्गीता)
- [Глава 1 — Arjuna Vishada Yoga](https://sa.wikisource.org/wiki/भगवद्गीता/अर्जुनविषादयोगः)
- [Глава 18 — Moksha Sannyasa Yoga](https://sa.wikisource.org/wiki/भगवद्_गीता_१८)

## Открытые данные

Для машинной обработки и будущего AI/RAG-модуля можно использовать открытый проект `gita/gita`, где Бхагавад-гита опубликована в JSON. Репозиторий использует Unlicense.

- [gita/gita — Bhagavad Gita in JSON](https://github.com/gita/gita)
- [Оригинальные стихи: data/verse.json](https://github.com/gita/gita/blob/main/data/verse.json)
- [Переводы: data/translation.json](https://github.com/gita/gita/blob/main/data/translation.json)
- [Главы: data/chapters.json](https://github.com/gita/gita/blob/main/data/chapters.json)

## Структура для KUBERA Learning

```text
docs/
└── bhagavad-gita.md
```

Следующий этап для полноценной библиотеки: добавить структурированные данные 18 глав в JSON/YAML с полями `chapter`, `verse`, `sanskrit`, `transliteration`, `translation`, `commentary`, `source` и `license`.
