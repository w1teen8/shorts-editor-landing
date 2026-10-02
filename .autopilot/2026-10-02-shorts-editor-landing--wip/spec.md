# Спецификация: лендинг-портфолио Daniil Zabolotnyi

## Задача

«Мне нужен одностраничный сайт, где клиент за минуту видит, какие ролики я монтирую, сколько это стоит и как работать со мной, — и сразу оставляет заявку». Видеомонтажёр вертикальных роликов (Reels, TikTok, Shorts) для экспертов, брендов и авторов.

## Решение

Один файл `index.html`, который открывается в любом браузере без сервера и сборки. Ниже — что получает пользователь, по разделам. Метки — строки манифеста.

### §1 Техника и доступность
- R01, R02 — одна страница, один файл: HTML, CSS в `<style>`, vanilla JS в `<script>`, без фреймворков и сборки.
- R03 — Google Fonts: Unbounded 500/700/800 для заголовков, Manrope 400–700 для текста.
- R04 — от 360 до 1440 px без горизонтальной прокрутки ни на одной ширине.
  - R04.1 — на 360 px логотип и «Book a call» помещаются в шапку в одну строку, а три карточки hero не вылезают за край.
- R05 — `.container`: max-width 1200 px, отступы по бокам 20 px.
- R06 — header/nav/main/section/footer. Всё кликабельное — настоящие `<button>` или `<a>`.
- R07 — у каждого поля есть `<label for>`. У кнопок без видимого текста есть aria-label: у карточек видео он есть, у иконок FAQ стоит `aria-hidden`.
- R08 — видимый `:focus-visible`: лаймовый на тёмном фоне, тёмный на лаймовом. При `prefers-reduced-motion` гаснут переходы, плавная прокрутка и подъём кнопок при наведении.
- R09.1 — нынешний `og:url` на сайт студии — выдуманный адрес этого лендинга, убрать в комментарий.
- R09 — meta description, og:type, og:title, og:description. `og:image` и `og:url` закомментированы как заглушки: адреса сайта в брифе нет.
- R10 — `lang="en"`, все тексты на английском.

### §2 Дизайн
- R11 — тёмная тема, CSS-переменные строго из брифа.
- R12 — заголовки и цифры на Unbounded: letter-spacing от −0.02 до −0.03em, крупные размеры через `clamp()`. Номера шагов тоже в этом диапазоне.
- R13 — у всех `.btn` border-radius 999px и min-height 48px.
- R14 — у карточек (`.card`, `.plan`) скругление 18–22px и рамка 1px `--line`.
- R15 — без градиентов и эмодзи. Play и галочка — inline SVG.
- R16 — секции разделены `border-top: 1px solid #222226`, сверху и снизу по 80px (на телефоне 64).

### §3 Карточка видео
- R17 — `<button class="reel" data-src data-poster>`: aspect-ratio 9/16, скругление 20px.
- R18 — тег ниши слева сверху, круглая play по центру, «[Your video]» внизу.
- R19 — тона фона по порядку tone-1…tone-6, цвета из брифа.
- R20 — если задан `data-poster`, появляется `<img loading="lazy" alt="">`, а подпись-заглушка скрывается.
- R21 — по клику создаётся `<video playsinline preload="none">` с `src` из `data-src` и запускается.
  - R21.1 — если видео не загрузилось или браузер отклонил `play()`, страница не бросает ошибок из JS, а карточка остаётся в исходном виде. Сетевую строку браузера «Failed to load resource» убрать нельзя (D01).
- R22 — одновременно играет только одно видео. Повторный клик ставит на паузу. Пока видео играет, play и подпись скрыты, а aria-label меняется с «Play …» на «Pause …».
- R23 — если `data-src` пустой, клик ничего не делает.

### §4 Шапка
- R24 — sticky-шапка с blur на полупрозрачном `--bg`. Логотип «Daniil Zabolotnyi.», точка лаймовая.
- R25, R63i — ссылки Work, Packages, Process, FAQ и кнопка «Book a call», которая ведёт на #contact. При ширине до 760px ссылки скрыты, видна кнопка. ASSUMPTION — логотип остаётся и на мобильном: «видна только кнопка» понимаю как «из навигации».

### §5 Hero
- R26 — две колонки, а при ширине до 900px одна.
- R27–R31 — бейдж с лаймовой точкой, H1 («to the end.» лаймом), лид, кнопки «Start a project» (accent, ведёт на #contact) и «See the work» (обводка, ведёт на #work), мелкая строка про сроки. Все тексты дословно из брифа.
- R32 — три карточки Expert / Brand / Creator со сдвигом по вертикали +24 / −16 / +32px.

### §6 Selected work
- R33 — eyebrow, H2 и текст справа (на узких экранах под заголовком), дословно.
- R34 — 6 колонок, при ширине до 1024px три, до 640px две.
- R35 — шесть карточек: ниша, название и цель, дословно и по порядку.

### §7 In every edit
- R36 — eyebrow «In every edit», H2 «Built for retention, not just to look nice».
- R37 — шесть карточек 01–06: Hook in the first 2 seconds / Animated captions / Pacing and cuts / Music and sound design / Color and look / Ready to post, и описанием в одно предложение. Описания говорят только о самом монтаже: без цифр, статистики и обещаний, которых нет в брифе. Сетка 3 → 2 → 1.

### §8 Packages
- R38 — eyebrow «Packages», H2 «Pick a volume, I handle the rest».
- R39 — Starter: «$160» + «· $40 per video»; «4 videos · up to 60 s each»; Hook, captions, music / 1 round of revisions / Delivery in 3–4 days / Cover frames included; кнопка «Choose Starter».
- R40 — Growth: карточка залита `--accent`, текст тёмный, бейдж «Most picked» (тёмная пилюля); «$390» + «/month»; «12 videos per month · ~$32 per video»; Everything in Starter / 2 rounds of revisions / Content plan and hook ideas / Priority turnaround; тёмная кнопка «Choose Growth».
- R41 — Custom: «from $500»; «Ads, launches, long-form to shorts»; Volume that fits your plan / Motion graphics on request / Podcast and webinar cutdowns / Fixed monthly slot; кнопка «Get a quote».
- R42 — «· $40 per video», «/month» и «from» — Manrope 15px (против 34–46px у цены), `white-space: nowrap`. Цена с припиской занимает одну строку на любой ширине от 360px.
- R43 — карточка тарифа — flex-колонка, кнопка прижата к низу.
- R44 — клик по кнопке тарифа записывает название в `input[name=package]` и ведёт к #contact.
  - A02 → R44 — в форме появляется строка «Selected package: Growth», чтобы клиент видел, что выбор сохранён.

### §9 How it works
- R45 — eyebrow «How it works», H2 «From raw footage to posted in four steps»; шаги Brief / Footage / Edit / Revisions & delivery.
- R62i — четыре шага с крупными лаймовыми номерами 01–04 и описанием в одно предложение. У Edit — «First draft in 48 hours». Остальные описания нейтральные, без названий сервисов. Сетка 4 → 2 → 1.

### §10 About
- R46 — круглая заглушка 120px с пунктирной рамкой «[Your photo]», H2 «Hi, I'm Daniil».
- R47 — «I edit short vertical videos for experts, small brands and creators. You work with me directly — no account managers, no handoffs.»
- R48 — заглушка «[Add 1–2 lines: experience, tools, niches]» и `<blockquote>` «[Client testimonial — add a real quote with the client's name and link]». Выдуманных отзывов нет.

### §11 FAQ
- R60i — eyebrow «FAQ» и H2 «Questions, answered». ASSUMPTION.
- R49 — `<details>/<summary>`, маркер браузера скрыт. Плюс в круге поворачивается на 45° и становится лаймовым.
- R50, R61i — пять вопросов дословно. Ответы:
  - *Do you film the videos too?* — `[Answer: do you film the videos, or only edit footage you send? — add your answer]`. Это факт о пользователе, и в брифе его нет.
  - *How fast do I get the first video?* — первый черновик за 48 часов после получения исходников, весь Starter за 3–4 дня.
  - *What if I don't like the edit?* — в каждый тариф входят раунды правок: 1 в Starter, 2 в Growth. Нужно оставить заметки, и Даниил переделает. Никаких «до бесконечности».
  - *Which music do you use?* — трендовые звуки или лицензированные треки, в зависимости от ролика.
  - *How do I pay?* — 50% вперёд и 50% при сдаче. Месячные планы оплачиваются в начале месяца. Card, PayPal, Wise или USDT.

### §12 Contact
- R51 — лаймовый блок со скруглением 28px, две колонки, при ширине до 900px одна.
- R52 — H2 и текст дословно.
- R53 — ссылки Telegram (`https://t.me/your_handle`), Instagram (`https://instagram.com/your_handle`) и Email (`mailto:you@email.com`), видимые заглушки `[@your_handle]` и `[you@email.com]`. Внешние ссылки открываются с `rel="noopener"`.
- R54 — форма: label «Your name» (required), label «Telegram or email» (required), textarea с label «Your account and what you need», `input type=hidden name=package` и тёмная кнопка «Send request».
  - R54.1 — пустые обязательные поля останавливает браузерная проверка, введённое не теряется.
- R55 — при пустом `action` форма не уходит. Появляется «Thanks! I'll get back to you within 24 hours.» (`role=status`), форма и выбранный тариф сбрасываются.
- R56 — HTML-комментарий над формой объясняет, куда вставить адрес Formspree. При заполненном `action` форма уходит обычным POST.

### §13 Footer
- R57 — две строки дословно. Ссылка на https://www.zabolotnyistudio.com/ открывается в новой вкладке.

### §14 Проверка
- R58 — Playwright на `file://`, ширины 1440 и 390 (плюс 360, 768 и 1024 для R04 и R34). На каждой ширине проверяется:
  - `scrollWidth == clientWidth`;
  - 0 ошибок в консоли;
  - цена с припиской занимает одну строку;
  - у каждой `.reel` высота/ширина = 16/9 ± 0.01;
  - число колонок `.work-grid` равно 6 / 3 / 2;
  - клик по тарифу заполняет hidden-поле;
  - submit показывает сообщение и сбрасывает форму.
- R59 — полностраничные скриншоты на 1440 и 390 плюс крупные кадры hero и тарифов на 390, в папке `screenshots/`.

## Решения по реализации

- Существующий `index.html` правится точечно, а не переписывается: он уже закрывает большинство строк, а `notes.md` перечисляет расхождения.
- Дополнительно, сверх брифа:
  - A01 → R08 — ссылка «Skip to content». Это доступность, ради R08.
  - A03 → R09 — `twitter:card` рядом с og-тегами. Без него ссылка в X выглядит хуже.
- Проверочный скрипт Playwright лежит вне проекта (scratchpad), в проект попадают только скриншоты. Проекту не нужен `package.json` ради одной проверки.

## Границы и швы

См. `interfaces.md`.

## Вне рамок

| Требование | Почему не сейчас |
|---|---|
| — | Ничего не отложено |

## Открытые места

Все заглушки видимые. От Даниила нужно:
- видео и обложки — заполнить `data-src` и `data-poster` у девяти карточек;
- ник в Telegram и Instagram, почта;
- фото, 1–2 строки об опыте, реальный отзыв;
- ответ на вопрос «Do you film the videos too?»;
- адрес Formspree для `action` формы;
- адрес сайта и картинка для `og:url` и `og:image`.
