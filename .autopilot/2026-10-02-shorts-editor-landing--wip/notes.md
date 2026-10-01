# Заметки по существующему коду

Записаны оркестратором: `index.html` собран в этой же сессии до запуска Autopilot, отдельная разведка не нужна.

## Что лежит в репозитории

- `index.html` (~690 строк): весь лендинг. `<style>` в `<head>`, `<script>` (IIFE) в конце `<body>`.
- `screenshots/`: снимки предыдущей проверки (1440 и 390). Будут перезаписаны.
- `prompt.md`: бриф пользователя.
- Сборки нет, зависимостей нет. Запуск — открыть файл в браузере.

## Устройство index.html

- Токены на `:root`: `--bg --card --line --divider(#222226) --text --soft --muted --accent --ink`, `--font-head` (Unbounded), `--font-body` (Manrope), `--radius-card: 20px`, `--header-h: 72px`.
- Порядок секций: `header.site-header` → `main#main` → `section.hero#top` → `section#work` → features (без id) → `section#packages` → `section#process` → about (без id) → `section#faq` → `section#contact` → `footer.site-footer`.
- Общие классы: `.container`, `.section` (border-top + padding 80/64), `.eyebrow`, `.h2`, `.section-head(--split)`, `.card`, `.btn` + `--accent | --outline | --dark`, `.accent`.
- Карточка видео: `button.reel.tone-1..6[data-src][data-poster][aria-label]` > `span.reel__tag`, `span.reel__play > svg`, `span.reel__caption`. Состояния: `.has-poster`, `.is-playing`. Медиа — `.reel__media` (img/video, absolute inset 0).
- Тарифы: `article.card.plan(.plan--accent)` > `.plan__badge`, `h3.plan__name`, `p.plan__price > span.plan__unit`, `p.plan__sub`, `ul.plan__list > li > svg`, `div.plan__cta > a.btn[data-package]`.
- Процесс: `ol.steps > li.card.step > .step__num + h3 + p`. Инлайн-стиль `style="list-style:none;…"` на `ol` — единственный в файле.
- FAQ: `.faq > details > summary(текст + span.faq__icon) + p.faq__answer`.
- Контакт: `.contact` (лаймовый grid) > левая колонка + `form.form[action=""]` с полями `#f-name`, `#f-contact`, `#f-message`, hidden `#f-package`, `p#f-package-note[hidden]`, `button[type=submit]`, `p.form__status[role=status]`.
- Брейкпоинты: 1024 (work 3 кол., features/steps 2), 900 (hero/contact 1 кол., тарифы стопкой, section-head в столбик), 760 (скрыт nav), 640 (телефон: work 2 кол., отступы 64).
- JS: (1) постеры и проигрывание карточек, общий `current` — одно видео за раз; (2) `[data-package]` → `#f-package` + видимая строка; (3) submit при пустом `action` → `preventDefault`, сообщение, `reset`.

## Расхождения с брифом, найденные при разборе

- Выдуманные факты о пользователе: «80% who watch on mute» (feature 02), «Google Drive, Dropbox» (шаг 02), ответ «No, I focus on editing… I'll share simple tips» (FAQ 1), «until it matches…» (FAQ 3 — обещает неограниченные правки при 1–2 раундах в тарифах), `og:url` указывает на сайт студии, а не на этот лендинг.
- `.step__num` letter-spacing −0.04em — вне диапазона брифа −0.02…−0.03.
- Инлайн-стиль на `ol.steps`.
- Ширина 360 px ни разу не проверялась.
