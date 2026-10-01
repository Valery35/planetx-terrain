# PlanetX terrain

Тайлы высот Марса и Луны для модуля QGIS
[PlanetX](https://github.com/Valery35/planetx). Модуль читает их
по одному тайлу по адресу
`https://raw.githubusercontent.com/Valery35/planetx-terrain/main/<тело>/{z}/{x}/{y}.png`.

| Папка | Тело | Источник | Уровни | Шаг высот |
|---|---|---|---|---|
| `mars` | Марс | NASA MGS MOLA MEGDR, 32 точки на градус, высоты над ареоидом | 0-5 | 10 м |
| `moon` | Луна | NASA LRO LOLA GDR, 64 точки на градус, высоты над сферой 1737.4 км | 0-5 | 20 м |

Тайлы - PNG 256×256 в сетке Web Mercator, порядок XYZ. Высота
в метрах записана как Terrarium: `R * 256 + G + B / 256 - 32768`.
Тайлы собирает `tools/build_body_terrain.py` хранилища PlanetX
из сеток PDS Geosciences Node.

В папке `imagery/<тело>/{z}/{x}/{y}.jpg` лежат снимки других тел:
Меркурия, Венеры, Юпитера, Ио, Европы, Ганимеда, Каллисто, Мимаса,
Энцелада, Тефии, Дионы, Реи, Титана, Япета, Цереры и Весты. Это JPEG 256×256 в сетке Web Mercator, порядок XYZ,
уровни 0-4, 0-5 или 0-6. Их нарезает `tools/build_body_imagery.py`
хранилища PlanetX из глобальных мозаик USGS Astrogeology
(planetarymaps.usgs.gov/mosaic) и NASA Photojournal (PIA07782 -
Юпитер, PIA17214 - Мимас). Список мозаик и подписи - в
`doc/SOURCES.md` хранилища PlanetX.

Данные NASA находятся в общественном достоянии. При показе
указывается источник: «NASA MGS MOLA MEGDR» для Марса и
«NASA LRO LOLA GDR» для Луны.

---

Mars and Moon elevation tiles for the QGIS plugin PlanetX. Terrarium
PNG tiles 256×256, Web Mercator XYZ, levels 0-5. Mars - NASA MGS MOLA
MEGDR, Moon - NASA LRO LOLA GDR, public domain NASA data.
