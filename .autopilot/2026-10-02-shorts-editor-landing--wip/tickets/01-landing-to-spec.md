# 01 — Лендинг строго по брифу, проверенный на пяти ширинах

**Требования:** R01, R02, R03, R04, R05, R06, R07, R08, R09, R10, R11, R12, R13, R14, R15, R16, R17, R18, R19, R20, R21, R22, R23, R24, R25, R26, R27, R28, R29, R30, R31, R32, R33, R34, R35, R36, R37, R38, R39, R40, R41, R42, R43, R44, R45, R46, R47, R48, R49, R50, R51, R52, R53, R54, R55, R56, R57, R58, R59, R60i, R61i, R62i, R63i, A01, A02, A03
**Зависит от:** —
**Зона:** `index.html` · `screenshots/`
**Волна:** 1
**Ревью:** нет
**Модель:** обычная

## Что должно заработать

Лендинг уже собран (`index.html`), но в нём есть выдуманные факты о Данииле и мелкие отступления от брифа. После таска страница говорит только то, что есть в брифе, а на месте недостающих фактов стоят видимые заглушки `[…]`. Каждое требование спецификации выполнено. Проверка в Playwright проходит на 360, 390, 768, 1024 и 1440 px, свежие скриншоты лежат в `screenshots/`.

Править точечно, не переписывать. Список расхождений — в `notes.md`, раздел «Расхождения с брифом». Контракты разметки — в `interfaces.md`, их не переименовывать.

## Из брифа, дословно

> «Сделай одностраничный лендинг-портфолио видеомонтажёра Daniil Zabolotnyi (монтаж Reels, TikTok, YouTube Shorts).»
> «Заголовки крупные, жирные, letter-spacing −0.02…−0.03em, размеры через clamp().»
> «Hook in the first 2 seconds / Animated captions / Pacing and cuts / Music and sound design / Color and look / Ready to post — к каждой короткое описание в одну строку.»
> «Четыре шага с крупными лаймовыми номерами: Brief / Footage / Edit (First draft in 48 hours) / Revisions & delivery.»
> «Do you film the videos too? / How fast do I get the first video? (48 hours, Starter pack 3–4 days) / What if I don't like the edit? / Which music do you use? (trending or licensed) / How do I pay? (50% upfront, 50% on delivery; monthly plans paid at the start of the month; Card, PayPal, Wise or USDT).»
> «Meta description и og-теги (og:image закомментирован как заглушка).»
> «Адаптив от 360px до 1440px, без горизонтальной прокрутки.»
> «открой страницу в Playwright на ширине 1440 и 390 px. Убедись, что нет горизонтальной прокрутки и ошибок в консоли, цены не переносятся некрасиво, а карточки 9:16 не искажаются. Пришли скриншоты.»

Весь бриф — `2026-10-02-brief.md`.

## Разделы спецификации

Всё в `spec.md`, §1–§14. Главное для правок: §1 (R04.1, R09.1), §2 (R12), §3 (R21.1), §7, §9, §11.

## Критерии приёмки

- [ ] В тексте страницы нет фактов, которых нет в брифе: ни «80%», ни «Google Drive», ни «Dropbox», ни «I focus on editing», ни «simple tips», ни обещания править «until it matches».
- [ ] Ответ на «Do you film the videos too?» — видимая заглушка `[Answer: do you film the videos, or only edit footage you send? — add your answer]`.
- [ ] Ответ на «What if I don't like the edit?» опирается на раунды правок из тарифов (1 в Starter, 2 в Growth), а не обещает бесконечные правки.
- [ ] Описания шести карточек «In every edit» и четырёх шагов — по одному предложению, без цифр, статистики и названий сервисов. У Edit — «First draft in 48 hours».
- [ ] Ответ про музыку говорит «trending or licensed» без лишних обещаний. Ответы про сроки и оплату совпадают с брифом.
- [ ] `og:url` больше не указывает на сайт студии: он закомментирован как заглушка, как и `og:image`.
- [ ] Ни один letter-spacing заголовка или цифры на Unbounded не выходит за −0.02…−0.03em (сейчас у номеров шагов −0.04em).
- [ ] В разметке нет атрибутов `style=""`.
- [ ] Playwright на 360, 390, 768, 1024 и 1440 px:
  - `scrollWidth == clientWidth`;
  - 0 ошибок в консоли и `pageerror`;
  - каждая `.plan__price` в одну строку;
  - у каждой `.reel` высота/ширина = 1.778 ± 0.01;
  - колонок в `.work-grid`: 6 на 1440, по 3 на 1024 и 768, по 2 на 390 и 360;
  - на 360 шапка в одну строку.
- [ ] Playwright: клик по «Choose Growth» → `input[name=package]` = «Growth», строка «Selected package: Growth» видна. Submit с заполненными обязательными полями → «Thanks! I'll get back to you within 24 hours.», поля пусты, hidden-поле пусто. Клик по карточке с пустым `data-src` не создаёт `<video>`.
- [ ] В `screenshots/` перезаписаны `shot-1440.png`, `shot-390.png`, `hero-390.png` и `pkg-390.png` с финальной версией. Добавлен `shot-360.png`.
- [ ] Всё, что уже соответствовало спецификации, осталось на месте: тексты из брифа дословно, цвета, сетки, поведение видео, форма.
