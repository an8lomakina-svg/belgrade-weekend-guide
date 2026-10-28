# Аудит изображений — 28 октября 2026

## Область и ограничения
Статический аудит index.html ветки main и дерева файлов GitHub. Прямое открытие GitHub Pages и реальная проверка naturalWidth/browser rendering не выполнены (нет доступа к опубликованной странице). Проверка внешних URL, фактических прав на фото и художественного соответствия не завершена. Числа ниже относятся к исходным 305 записям до runtime-фильтра завершённых событий.

## Итоги
- 305 записей исходного каталога.
- 44 записи не имеют отдельного назначения в handPaintedArtworks, commonsPhotos или photos.
- 250 записей имеют запись в handPaintedArtworks; 21 — commonsPhotos; 1 — photos; пересечения возможны.
- Все пути handPaintedArtworks ведут к существующим GitHub-файлам на момент проверки.
- 260 файлов внутри assets/illustrations, 333 МБ суммарно, из них 82 файла более 2 МБ и 65 более 3 МБ.
- Браузерный fallback при загрузочной ошибке использует knitArt(), а не индивидуальную гуашевую иллюстрацию.
- Неиспользуемые файлы: aviation-museum-gouache.png, belgrade-kalemegdan-panorama-gouache.png, belgrade-pobednik-gouache.png.

## Без индивидуального визуала (44)
### museums (2)
- Музей Сербского медицинского общества
- Музей прикладного искусства

### creative (3)
- Clay & Tiramisu
- Ametrin
- Twentyfive Market

### games (2)
- KartLand
- Cineplexx Galerija

### food (3)
- Dolcino Miljakovac
- Puter Fine Bistro
- Bistro Mali Pijac

### coffee (10)
- Verde Brunch & More — Дединье
- Kafedžinica — Врачар
- Bloom — бранч на Дорчоле
- Kuća čaja
- Mimosa
- Lumi Specialty Coffee
- Užitak Coffee Selection & Delights
- Kofilin — Carice Milice
- PASTIS Bistro
- Simbol Specialty Coffee

### tours (1)
- Музей иллюзий — экскурсия с гидом

### design (5)
- Muzej čokolade
- Muzej automobila
- Muzej nauke i tehnike
- Muzej Jugoslavije
- Muzej vazduhoplovstva

### events (15)
- Вукобратовичевы дни робототехники
- Танцевальные киновечера: «Бурная погода»
- Klaber — фильм
- Molière — французский мюзикл
- Goca Tržan
- Yasmin Levy — One More Night
- Željko Vasić — 25 лет на сцене
- Tommy Emmanuel
- Uriah Heep — The Magician’s Farewell
- Sarah Brightman — A Winter Symphony
- the Chaika — «Я в порядке!»
- QUEEN SYMPHONY SENSATION
- Ruka pravde — премьера фильма
- Paleto — рисование «Тоскана», 22 октября
- Boya Porcelain — чашка и блюдце, 22 октября

### boats (3)
- Круиз по Саве и Дунаю с гидом
- Закатный круиз с гидом
- Частный двухчасовой круиз

## План исправлений
1. Для каждого объекта искать официальное фото с доказанными правами, проверять соответствие и загрузку.
2. Если разрешённое фото не найдено — создать отдельную индивидуальную иллюстрацию (не использовать генератор knitArt как замену).
3. Добавить проверку, запрещающую публикацию новых карточек без визуала и отслеживающую ошибки naturalWidth после появления в viewport.
4. Оптимизировать тяжёлые файлы и измерить загрузку на мобильном соединении.
5. Пройти все видимые категории и модальное окно афиши в Safari iPhone; зафиксировать screenshots, URL, естественную ширину и статус изображений.

## Статус
Статическая часть выполнена. Полный end-to-end аудит опубликованной версии НЕ выполнен. Нельзя считать карточки проверенными в браузере по одному наличию пути.
