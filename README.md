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

Данные NASA находятся в общественном достоянии. При показе
указывается источник: «NASA MGS MOLA MEGDR» для Марса и
«NASA LRO LOLA GDR» для Луны.

---

Mars and Moon elevation tiles for the QGIS plugin PlanetX. Terrarium
PNG tiles 256×256, Web Mercator XYZ, levels 0-5. Mars - NASA MGS MOLA
MEGDR, Moon - NASA LRO LOLA GDR, public domain NASA data.
