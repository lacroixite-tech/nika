# NIKA — Visual Identity & Character Consistency

Практическое дополнение к [NIKA_BIBLE.md](NIKA_BIBLE.md): что зафиксировано на референсах
и как удерживать консистентность персонажа при генерации.

## Референсы

| Файл | Что это | Для чего использовать |
|---|---|---|
| [`references/nika-moodboard.webp`](../references/nika-moodboard.webp) | Мудборд / character sheet | Канон: лицо, гардероб, аксессуары, палитра, типографика |
| [`references/nika-window-profile.webp`](../references/nika-window-profile.webp) | Профиль ¾, окно, вечерний город, кружка | Основной lifestyle-кадр, освещение «синий час» |
| [`references/nika-window-portrait.webp`](../references/nika-window-portrait.webp) | Взгляд в камеру, тот же сет | Face-reference для обложек и talking-head |

## Canon — лицо и тело

- 27–30 лет, рост ~168 см, спортивное функциональное телосложение.
- Прямое тёмное каре до линии челюсти / до плеч, лёгкая небрежность прядей.
- Серо-зелёные глаза, спокойный наблюдающий взгляд, без улыбки «для камеры».
- Естественная кожа: видимая текстура, **лёгкие веснушки** на носу и скулах (зафиксированы на фото 2–3).
- Без «AI-идеальности»: никакого пластикового ретуша, гипертрофированных губ, глянца.

## Canon — гардероб и аксессуары

| Элемент | Детали |
|---|---|
| Техническая куртка | Чёрная/графитовая, мятая мембранная ткань, стойка-воротник с капюшоном, **оранжевая светящаяся линия** по воротнику, плечу и молнии; ремень-стропа с пряжкой на груди |
| База | Белая / светло-серая футболка, у лабораторного образа — серый high-neck |
| Брюки | Чёрные карго с оранжевыми акцентами на швах |
| Lab coat | Белый футуристичный халат с оранжевой линией и логотипом на груди, чёрные нитриловые перчатки |
| Наушник | Одно ухо, open-ear / bone-conduction, с **оранжевым индикатором** |
| Кулон | Тонкий чёрный шнур, вертикальный светящийся оранжевый стержень |
| Прочее | Sling-сумка с логотипом, минималистичные светло-серые кроссовки, тактический ремень, фитнес-браслет, стилус |
| Логотип | Треугольник/гора из тонких линий (Λ-символ) — на груди, сумке, халате |

**Правило оранжевой линии (Human Signal):** она всегда тонкая, одна-две линии в кадре,
никогда не заливка и не неон-киберпанк. Это сигнал, а не декор.

## Canon — окружение

«Исследовательская станция будущего в обычной российской квартире»:

- панорамное окно на вечерний многоэтажный город (синий час, тёплые огни окон);
- стеллажи с книгами и коробками, вьющиеся растения, тёплая подсветка полок;
- стеклянная HUD-панель с мозгом, графиками и волной сигнала;
- рабочий стол с ноутбуком, рядом — кровать (реальная квартира, не студия);
- постер «SMALL STEPS / BIG SYSTEMS»;
- чёрная матовая кружка — повторяющийся предмет.

## Палитра

| Токен | Роль | Ориентир HEX |
|---|---|---|
| Graphite | человеческая система, фон, одежда | `#1C1D1F` / `#3A3C40` |
| White | evidence, текст, база | `#F2F2F0` |
| Orange | signal — только акценты | `#FF6A1A` |
| Soft blue | recovery, небо, ночные сцены | `#8FA8C8` |
| Light gray | вспомогательный | `#A6A8AB` |

HEX — рабочие ориентиры по референсам; уточнить при создании гайда для дизайнера.

## Типографика и графика

- Речь / заголовки: современный grotesk, тонкое начертание, капс для меток (`HUMAN SIGNAL`, `CLINICAL × CYBERNETIC × HUMAN`).
- Данные: моноширинный шрифт (`ENERGY 72%`, координаты `55.7558° N 37.6173° E`).
- Тонкие линии, много воздуха, короткие оранжевые штрихи-разделители, ЭКГ-волна как иконка сигнала.
- Микротексты в духе мудборда: «Тонкая линия. Сигнал. Ты здесь.», «Тихая точность. Польза. Гармония.», «FUNCTION OVER APPEARANCE».

## Базовый промпт для генерации (EN)

```
Photorealistic portrait of NIKA, a 28-year-old woman, digital health engineer.
Straight near-black chin-length bob, slightly messy strands, grey-green eyes,
natural skin texture with light freckles, calm observant expression, no smile.
Athletic functional build. Wearing a black crinkled technical membrane jacket
with a high collar and hood, a thin glowing orange interface line along the
collar, shoulder and zipper, chest strap with buckle, plain white t-shirt,
thin black cord necklace with a vertical glowing orange bar pendant,
single open-ear earpiece with a small orange LED. Holding a matte black mug.
Setting: ordinary Russian high-rise apartment turned near-future research
station — floor-to-ceiling window, dusk city with lit windows, bookshelves
with warm shelf lighting, trailing plants, translucent glass HUD panel with a
brain scan and a signal waveform, desk with laptop.
Blue-hour lighting, soft cool ambient light with warm practical lights,
cinematic, shallow depth of field, 35mm, muted graphite palette with orange
accents. clinical x cybernetic x human.
```

**Negative:** `plastic skin, heavy retouch, glamour makeup, big smile, neon cyberpunk overload,
fitness-model body, oversaturated colors, cluttered orange, text artifacts, extra fingers`

Для консистентности лица всегда подавать `nika-window-portrait.webp` как face/character reference.

## Открытые вопросы

- **PROMETHEUS** на мудборде — название исходной системы/лаборатории, создавшей НИКУ? Зафиксировать в backstory или убрать.
- Координаты `55.7558° N 37.6173° E` (центр Москвы) — осознанная привязка локации к Москве?
- Нужен ли голос (TTS/voice clone) и его описание: тембр, темп, интонация.
