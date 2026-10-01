# Манифест требований

Источник: `2026-10-02-brief.md`. Строку из этого списка может снять **только пользователь**.

| ID | Из брифа (дословно) | Статус | Основание | Где |
|----|---------------------|--------|-----------|-----|
| R01 | «одностраничный лендинг-портфолио видеомонтажёра Daniil Zabolotnyi (монтаж Reels, TikTok, YouTube Shorts)» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R02 | «Один файл index.html: HTML + CSS в <style> + vanilla JS в <script>. Без фреймворков и сборки.» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R03 | «Шрифты Google Fonts: Unbounded (500/700/800) для заголовков, Manrope (400–700) для текста.» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R04 | «Адаптив от 360px до 1440px, без горизонтальной прокрутки.» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R05 | «Контейнер max-width 1200px, боковые отступы 20px.» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R06 | «header/nav/main/section/footer, настоящие <button> и <a>» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R07 | «<label> у полей, aria-label у кнопок только с иконкой» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R08 | «видимый :focus-visible, prefers-reduced-motion» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R09 | «Meta description и og-теги (og:image закомментирован как заглушка).» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R10 | «Язык сайта английский (lang="en"). Все тексты на странице на английском.» | in-ticket | в брифе однозначно — решения не требуется | spec §1 → T01 |
| R11 | «Тёмная тема. CSS-переменные: --bg #0E0E10, --card #17171A, --line #26262B, --text #F2F0EA, --soft #C9C7C0, --muted #A8A6A0, --accent #D4FF3A (лайм).» | in-ticket | в брифе однозначно — решения не требуется | spec §2 → T01 |
| R12 | «Заголовки крупные, жирные, letter-spacing −0.02…−0.03em, размеры через clamp().» | in-ticket | в брифе однозначно — решения не требуется | spec §2 → T01 |
| R13 | «Кнопки-«пилюли» (border-radius 999px), высота ≥ 48px.» | in-ticket | в брифе однозначно — решения не требуется | spec §2 → T01 |
| R14 | «Карточки со скруглением 18–22px и тонкой рамкой.» | in-ticket | в брифе однозначно — решения не требуется | spec §2 → T01 |
| R15 | «Никаких градиентов, эмодзи и стоковых иконок. Иконки (play, галочка) — inline SVG.» | in-ticket | в брифе однозначно — решения не требуется | spec §2 → T01 |
| R16 | «Секции разделены линией border-top 1px #222226, вертикальные отступы около 80px.» | in-ticket | в брифе однозначно — решения не требуется | spec §2 → T01 |
| R17 | «<button class="reel" data-src="" data-poster="">, пропорции 9:16 (aspect-ratio), скругление 20px.» | in-ticket | в брифе однозначно — решения не требуется | spec §3 → T01 |
| R18 | «тег ниши в левом верхнем углу, круглая кнопка play по центру, подпись-заглушка «[Your video]» внизу.» | in-ticket | в брифе однозначно — решения не требуется | spec §3 → T01 |
| R19 | «Пока видео нет, фон — один из 6 приглушённых тонов: #2A2433, #1E2B2A, #33281F, #22263A, #2E2A1C, #2B1F27.» | in-ticket | в брифе однозначно — решения не требуется | spec §3 → T01 |
| R20 | «если задан data-poster, показывать <img loading="lazy">.» | in-ticket | в брифе однозначно — решения не требуется | spec §3 → T01 |
| R21 | «По клику создавать <video playsinline preload="none"> из data-src и запускать.» | in-ticket | в брифе однозначно — решения не требуется | spec §3 → T01 |
| R22 | «Одновременно играет только одно видео. Повторный клик ставит на паузу.» | in-ticket | в брифе однозначно — решения не требуется | spec §3 → T01 |
| R23 | «Если data-src пустой, ничего не делать.» | in-ticket | в брифе однозначно — решения не требуется | spec §3 → T01 |
| R24 | «Sticky-шапка с blur-фоном: логотип «Daniil Zabolotnyi.» (точка акцентным цветом)» | in-ticket | в брифе однозначно — решения не требуется | spec §4 → T01 |
| R25 | «ссылки Work, Packages, Process, FAQ; кнопка «Book a call» → #contact. На мобильном видна только кнопка.» | in-ticket | в брифе однозначно — решения не требуется | spec §4 → T01 |
| R26 | «Hero, две колонки (на мобильном одна)» | in-ticket | в брифе однозначно — решения не требуется | spec §5 → T01 |
| R27 | «бейдж «Reels · TikTok · Shorts editor» с лаймовой точкой» | in-ticket | в брифе однозначно — решения не требуется | spec §5 → T01 |
| R28 | «H1 «Short videos people watch to the end.» (слова «to the end.» акцентным цветом)» | in-ticket | в брифе однозначно — решения не требуется | spec §5 → T01 |
| R29 | «лид: «I turn your raw footage into vertical videos with a strong hook, tight pacing, captions and sound — ready to post on Instagram, TikTok and YouTube Shorts.»» | in-ticket | в брифе однозначно — решения не требуется | spec §5 → T01 |
| R30 | «кнопки «Start a project» (accent) и «See the work» (обводка)» | in-ticket | в брифе однозначно — решения не требуется | spec §5 → T01 |
| R31 | «мелкая строка: «Reply within 24 hours · First draft in 48 hours»» | in-ticket | в брифе однозначно — решения не требуется | spec §5 → T01 |
| R32 | «справа три карточки видео (Expert, Brand, Creator) со смещением по вертикали: +24px, −16px, +32px.» | in-ticket | в брифе однозначно — решения не требуется | spec §5 → T01 |
| R33 | «#work «Selected work», H2 «Edits for experts, brands and creators», справа текст «Tap a video to play it with sound. Each card shows the niche and what the edit was built to do.»» | in-ticket | в брифе однозначно — решения не требуется | spec §6 → T01 |
| R34 | «Сетка из 6 карточек видео: 6 колонок на десктопе, 3 на планшете, 2 на телефоне.» | in-ticket | в брифе однозначно — решения не требуется | spec §6 → T01 |
| R35 | «Под каждой название и цель: Expert — Talking-head explainer — Hook + captions for a coach; Brand — Product showcase — Fast cuts for a launch; Food — Café menu reel — Sound-led b-roll edit; Fitness — Workout tips — Text overlays, beat sync; Real estate — Apartment tour — Smooth walkthrough; Podcast — Podcast clip — Best moment, cut to 30s.» | in-ticket | в брифе однозначно — решения не требуется | spec §6 → T01 |
| R36 | «"In every edit", H2 «Built for retention, not just to look nice». Шесть карточек с номерами 01–06» | in-ticket | в брифе однозначно — решения не требуется | spec §7 → T01 |
| R37 | «Hook in the first 2 seconds / Animated captions / Pacing and cuts / Music and sound design / Color and look / Ready to post — к каждой короткое описание в одну строку.» | in-ticket | в брифе однозначно — решения не требуется | spec §7 → T01 |
| R38 | «#packages «Packages», H2 «Pick a volume, I handle the rest». Три тарифа» | in-ticket | в брифе однозначно — решения не требуется | spec §8 → T01 |
| R39 | «Starter — «$160 · $40 per video» — 4 videos · up to 60 s each — Hook, captions, music; 1 round of revisions; Delivery in 3–4 days; Cover frames included — кнопка «Choose Starter».» | in-ticket | в брифе однозначно — решения не требуется | spec §8 → T01 |
| R40 | «Growth (лаймовая карточка, бейдж «Most picked») — «$390/month» — 12 videos per month · ~$32 per video — Everything in Starter; 2 rounds of revisions; Content plan and hook ideas; Priority turnaround — кнопка «Choose Growth».» | in-ticket | в брифе однозначно — решения не требуется | spec §8 → T01 |
| R41 | «Custom — «from $500» — Ads, launches, long-form to shorts — Volume that fits your plan; Motion graphics on request; Podcast and webinar cutdowns; Fixed monthly slot — кнопка «Get a quote».» | in-ticket | в брифе однозначно — решения не требуется | spec §8 → T01 |
| R42 | «Приписки «· $40 per video» и «/month» набраны мелким шрифтом Manrope, white-space: nowrap.» | in-ticket | в брифе однозначно — решения не требуется | spec §8 → T01 |
| R43 | «Кнопки прижаты к низу карточки.» | in-ticket | в брифе однозначно — решения не требуется | spec §8 → T01 |
| R44 | «Клик по кнопке записывает название тарифа в скрытое поле формы и ведёт к #contact.» | in-ticket | в брифе однозначно — решения не требуется | spec §8 → T01 |
| R45 | «#process «How it works», H2 «From raw footage to posted in four steps». Четыре шага с крупными лаймовыми номерами: Brief / Footage / Edit (First draft in 48 hours) / Revisions & delivery.» | in-ticket | в брифе однозначно — решения не требуется | spec §9 → T01 |
| R46 | «About: круглая заглушка «[Your photo]» 120px с пунктирной рамкой, H2 «Hi, I'm Daniil».» | in-ticket | в брифе однозначно — решения не требуется | spec §10 → T01 |
| R47 | «Текст: «I edit short vertical videos for experts, small brands and creators. You work with me directly — no account managers, no handoffs.»» | in-ticket | в брифе однозначно — решения не требуется | spec §10 → T01 |
| R48 | «заглушка «[Add 1–2 lines: experience, tools, niches]» и blockquote-заглушка «[Client testimonial — add a real quote with the client's name and link]». Выдуманные отзывы не писать.» | in-ticket | в брифе однозначно — решения не требуется | spec §10 → T01 |
| R49 | «#faq на <details>/<summary>, плюсик поворачивается на 45° при открытии.» | in-ticket | в брифе однозначно — решения не требуется | spec §11 → T01 |
| R50 | «Do you film the videos too? / How fast do I get the first video? (48 hours, Starter pack 3–4 days) / What if I don't like the edit? / Which music do you use? (trending or licensed) / How do I pay? (50% upfront, 50% on delivery; monthly plans paid at the start of the month; Card, PayPal, Wise or USDT).» | in-ticket | в брифе однозначно — решения не требуется | spec §11 → T01 |
| R51 | «#contact: большой лаймовый блок со скруглением 28px, две колонки.» | in-ticket | в брифе однозначно — решения не требуется | spec §12 → T01 |
| R52 | «H2 «Let's make your next reel.», текст «Tell me about your account and send a link to the footage. I'll reply within 24 hours with an estimate.»» | in-ticket | в брифе однозначно — решения не требуется | spec §12 → T01 |
| R53 | «ссылки на Telegram, Instagram и Email с заглушками [@your_handle] и [you@email.com].» | in-ticket | в брифе однозначно — решения не требуется | spec §12 → T01 |
| R54 | «форма: Your name, Telegram or email (оба required), textarea «Your account and what you need», скрытое поле package, тёмная кнопка «Send request».» | in-ticket | в брифе однозначно — решения не требуется | spec §12 → T01 |
| R55 | «Если у формы пустой action, по submit показывать «Thanks! I'll get back to you within 24 hours.» и сбрасывать форму.» | in-ticket | в брифе однозначно — решения не требуется | spec §12 → T01 |
| R56 | «Добавь комментарий, куда вставить адрес Formspree.» | in-ticket | в брифе однозначно — решения не требуется | spec §12 → T01 |
| R57 | «Footer: «© 2026 Daniil Zabolotnyi · Reels & TikTok editing» и «Part of Zabolotnyi Studio» со ссылкой на https://www.zabolotnyistudio.com/.» | in-ticket | в брифе однозначно — решения не требуется | spec §13 → T01 |
| R58 | «открой страницу в Playwright на ширине 1440 и 390 px. Убедись, что нет горизонтальной прокрутки и ошибок в консоли, цены не переносятся некрасиво, а карточки 9:16 не искажаются.» | in-ticket | в брифе однозначно — решения не требуется | spec §14 → T01 |
| R59 | «Пришли скриншоты.» | in-ticket | в брифе однозначно — решения не требуется | spec §14 → T01 |
| R60i | *(подразумевается)* заголовок секции FAQ — в брифе для #faq не задан H2, а у остальных секций он есть | in-ticket | ASSUMPTION — принято за пользователя: нейтральный заголовок «Questions, answered» (не факт о Данииле, просто текст секции) | spec §11 → T01 |
| R61i | *(подразумевается)* ответы на 5 вопросов FAQ — бриф даёт только суть для трёх из них | in-ticket | Ответы собираются только из брифа: сроки (48 ч, 3–4 дня), правки (1–2 раунда из тарифов), музыка (trending or licensed), оплата. Снимает ли Даниил сам — факт о пользователе, в брифе его нет → видимая заглушка «[Answer: do you film or only edit?]». Без выдуманной статистики | spec §11 → T01 |
| R62i | *(подразумевается)* описания 4 шагов процесса — в брифе только названия (кроме Edit) | in-ticket | ASSUMPTION — принято за пользователя: короткие описания шагов без конкретных сервисов и обещаний, которых нет в брифе (кроме «First draft in 48 hours» из брифа) | spec §9 → T01 |
| R63i | *(подразумевается)* «Book a call» ведёт на форму, а не на календарь — отдельной ссылки на созвон в брифе нет | in-ticket | Бриф прямо задаёт «Book a call» → #contact; отдельного календаря нет. ASSUMPTION — принято за пользователя: созвон договаривается через форму | spec §4 → T01 |
