+++
title = 'My'
date = 2024-07-20T23:05:30+03:00
draft = false
tags = ["my"]
+++

Шаги для настройки цветов

  1.  Создайте файл CSS для кастомизации цветов:
  • Создайте файл theme-vars-override.css в директории assets/css/extended/ вашего проекта Hugo.
  2.  Добавьте кастомные цвета:
  • В этот файл можно добавить CSS переменные для настройки различных элементов темы. Пример кода:

```css
:root {
    --theme: #ffffff; /* Основной фон */
    --entry: #f0f0f0; /* Вторичный фон */
    --primary: #007bff; /* Основной цвет */
    --secondary: #6c757d; /* Дополнительный цвет */
    --tertiary: #e9ecef; /* Третичный цвет */
    --content: #212529; /* Цвет текста */
    --hljs-bg: #1e1e1e; /* Фон для подсветки синтаксиса */
    --code-bg: #f8f9fa; /* Фон для кода */
    --border: #dee2e6; /* Цвет границ */
}

.dark {
    --theme: #343a40; /* Темный фон */
    --entry: #495057; /* Вторичный темный фон */
    --primary: #adb5bd; /* Основной цвет для темной темы */
    --secondary: #6c757d; /* Дополнительный цвет для темной темы */
    --tertiary: #ced4da; /* Третичный цвет для темной темы */
    --content: #f8f9fa; /* Цвет текста для темной темы */
    --hljs-bg: #2e2e33; /* Фон для подсветки синтаксиса в темной теме */
    --code-bg: #37383e; /* Фон для кода в темной теме */
    --border: #495057; /* Цвет границ для темной темы */
}
```

Для создания гармоничных цветовых схем можно использовать онлайн-инструменты, такие как:

  • Coolors: Coolors.co
  • Adobe Color: Adobe Color
  • Paletton: Paletton
  • Color Hunt: Color Hunt

Для каждой палитры (Latte, Frappé, Macchiato, Mocha) адаптируем CSS с цветами для Hugo PaperMod. Вот пример:


```css
.latte {
    --color-bg: #eff1f5;
    --color-primary: #007bff;
    --color-secondary: #6c757d;
    --color-tertiary: #ccd0da;
    --color-text: #4c4f69;
    --color-hljs-bg: #e6e9ef;
    --color-code-bg: #f5f5f5;
    --color-border: #dee2e6;
    
    /* Подсветка синтаксиса */
    --color-syntax-bg: #ffffff;
    --color-syntax-text: #4c4f69;
    --color-syntax-keyword: #007bff;
    --color-syntax-string: #a6d189;
    --color-syntax-function: #1e66f5;
    --color-syntax-comment: #7c7f93;
    --color-syntax-variable: #ca9ee6;
}

.frappe {
    --color-bg: #303446;
    --color-primary: #007bff;
    --color-secondary: #6c757d;
    --color-tertiary: #414559;
    --color-text: #c6d0f5;
    --color-hljs-bg: #292c3c;
    --color-code-bg: #37383e;
    --color-border: #495057;
    
    /* Подсветка синтаксиса */
    --color-syntax-bg: #303446;
    --color-syntax-text: #c6d0f5;
    --color-syntax-keyword: #8caaee;
    --color-syntax-string: #a6d189;
    --color-syntax-function: #85c1dc;
    --color-syntax-comment: #737994;
    --color-syntax-variable: #f5a97f;
}

.macchiato {
    --color-bg: #303446;
    --color-primary: #007bff;
    --color-secondary: #6c757d;
    --color-tertiary: #414559;
    --color-text: #c6d0f5;
    --color-hljs-bg: #292c3c;
    --color-code-bg: #37383e;
    --color-border: #495057;
    
    /* Подсветка синтаксиса */
    --color-syntax-bg: #303446;
    --color-syntax-text: #c6d0f5;
    --color-syntax-keyword: #ca9ee6;
    --color-syntax-string: #a6d189;
    --color-syntax-function: #8caaee;
    --color-syntax-comment: #737994;
    --color-syntax-variable: #f5a97f;
}

.macchiato {
    --color-bg: #303446;
    --color-primary: #007bff;
    --color-secondary: #6c757d;
    --color-tertiary: #414559;
    --color-text: #c6d0f5;
    --color-hljs-bg: #292c3c;
    --color-code-bg: #37383e;
    --color-border: #495057;
    
    /* Подсветка синтаксиса */
    --color-syntax-bg: #303446;
    --color-syntax-text: #c6d0f5;
    --color-syntax-keyword: #ca9ee6;
    --color-syntax-string: #a6d189;
    --color-syntax-function: #8caaee;
    --color-syntax-comment: #737994;
    --color-syntax-variable: #f5a97f;
}

```


```toml
[markup]
  [markup.highlight]
    noClasses = false
    style = "monokai" # Здесь вы можете указать стиль подсветки, например, "monokai"
    lineNoStart = 1
    lineNos = true
    lineNumbersInTable = true
```
