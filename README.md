# PlanetX terrain

Данные модуля QGIS [PlanetX](https://github.com/Valery35/planetx)
и программы [PlanetX Lite](https://github.com/Valery35/planetx-lite):
снимки тел, плиты, палеогеография, каталог Рамсея, демо, шрифты, карта
неба. Модуль и Lite читают их по адресу
`https://raw.githubusercontent.com/Valery35/planetx-terrain/main/<путь>`.

Высоты Марса и Луны отсюда убраны 25 октября 2026 года. Теперь они
подробнее, уровни 0-7, в хранилище
[planetx-bodies-terrain](https://github.com/Valery35/planetx-bodies-terrain),
снимки Марса и Луны - в
[planetx-bodies-imagery](https://github.com/Valery35/planetx-bodies-imagery).
В папке `imagery/<тело>/{z}/{x}/{y}.jpg` лежат снимки других тел:
Меркурия, Венеры, Юпитера, Ио, Европы, Ганимеда, Каллисто, Мимаса,
Энцелада, Тефии, Дионы, Реи, Титана, Япета, Цереры и Весты. Это JPEG 256×256 в сетке Web Mercator, порядок XYZ,
уровни 0-4, 0-5 или 0-6. Их нарезает `tools/build_body_imagery.py`
хранилища PlanetX из глобальных мозаик USGS Astrogeology
(planetarymaps.usgs.gov/mosaic) и NASA Photojournal (PIA07782 -
Юпитер, PIA17214 - Мимас). Список мозаик и подписи - в
`doc/SOURCES.md` хранилища PlanetX.

В папке `slab2/<код>.npz` лежат погружающиеся плиты 27 зон
субдукции по модели USGS Slab2 (Hayes, 2018, doi:10.5066/F7PV6JNV).
В файле зоны - глубина верхней поверхности плиты, толщина и падение
на сетке 0.1°, узлы вне контура зоны USGS удалены. Файлы собирает
`tools/build_slabs.py` хранилища PlanetX из архива
Slab2Distribute_Mar2018.tar.gz. Модуль запрашивает файл зоны, когда
разрез Земли её касается. Данные USGS находятся в общественном
достоянии США, при показе указывается «Slabs: USGS Slab2».

В папке `paleo/merdith2021/<возраст>.png` лежат карты суши прошлого
на возрасты от 0 до 1000 млн лет с шагом 5. Это PNG в один бит
на пиксель, 8192×4096, равнопромежуточная проекция, долгота -180
слева, север вверху, суша белая. Карты собирает `tools/build_paleo.py`
хранилища PlanetX из берегов модели Merdith et al. 2021
(Earth-Science Reviews 214, 103477), полученных через веб-службу
GPlates (EarthByte, AuScope). Модель опубликована по CC BY 4.0,
zenodo.org/records/4485738. Узкие замкнутые полосы воды между кусками
суши закрашены сушей. Указатель возрастов - `index.json`. При показе
указывается «Paleogeography: GPlates Web Service, Merdith et al. 2021».

---

Data of the QGIS plugin PlanetX and PlanetX Lite. Mars and Moon heights
moved on 25 October 2026 to planetx-bodies-terrain (levels 0-7), Mars and
Moon imagery is in planetx-bodies-imagery.
Folder `slab2` holds subducting slabs of 27 zones from USGS Slab2
(Hayes, 2018), public domain USGS data.
Folder `paleo/merdith2021` holds 1-bit land maps for 0-1000 Ma in 5 Ma steps,
built from the Merdith et al. 2021 model (CC BY 4.0) via the GPlates Web Service.

В папке `rumsey` лежит каталог привязанных карт коллекции Дэвида Рамсея
для окна «Карты Рамсея» модуля. `index.json` - все 56 618 карт: номер,
рамка (запад, юг, восток, север), год, название, масштаб и клетка.
`cells/<широта>_<долгота>.json` - подробности карт по клеткам 10° по
середине рамки: адрес изображения IIIF, способ привязки, опорные точки
и обрезка поля карты в пикселях. Каталог собирает `tools/build_rumsey.py`
хранилища PlanetX из набора Стэнфорда «David Rumsey Map Collection:
Georeferenced Maps Metadata» (purl.stanford.edu/ss311gz1992, CC0).
Изображений карт здесь нет, модуль собирает их у пользователя из службы
IIIF коллекции. Изображения коллекции - CC BY-NC-SA 3.0.

В папке `demo` лежат демо модуля PlanetX и программы
[PlanetX Lite](https://github.com/Valery35/planetx-lite): сцены
`*.planetx` и их крупные файлы - растры высот, слои GeoPackage,
3D-модели. Раскладка та же, что в папке `planetx/demo` модуля. Модуль
и Lite берут файл по адресу
`https://raw.githubusercontent.com/Valery35/planetx-terrain/main/demo/<путь>`,
когда открывается демо, и хранят его у себя. Сцены и файлы демо -
GNU GPL 3 (`demo/LICENSE`), у чужих данных внутри свои условия -
`demo/SOURCES.md`. Лицензия папки `demo` не распространяется
на остальные папки хранилища.

Folder `demo` holds PlanetX and PlanetX Lite demo scenes and their
large files, GNU GPL 3, third-party terms in `demo/SOURCES.md`.

В папке `fonts` лежат шрифты Noto Sans SC, JP и KR для страницы
PlanetX Lite на китайском, японском и корейском. Это обычное начертание
переменных шрифтов Google Fonts (github.com/google/fonts, папки
`ofl/notosanssc`, `notosansjp`, `notosanskr`), урезанное до знаков
GB2312, JIS X 0208 и хангыля KS X 1001. Шрифты - SIL Open Font License
1.1, текст - `fonts/OFL.txt`. Страница скачивает шрифт при первом
выборе такого языка, программа берёт шрифт системы.

Folder `fonts` holds Noto Sans SC, JP and KR, the regular weight of the
Google Fonts variable fonts subset to GB2312, JIS X 0208 and KS X 1001
Hangul, SIL Open Font License 1.1 (`fonts/OFL.txt`), for the PlanetX
Lite web page.

В папке `sky/starmap` лежит карта неба NASA SVS Deep Star Maps 2020
(starmap_2020_32k, svs.gsfc.nasa.gov/4851) тайлами HiPS - JPEG 512×512
в сетке HEALPix, порядки 0-4, `Norder3/Allsky.jpg` и `properties`.
Яркость тайлов - та же, что у картинки Млечного пути модуля. Тайлы
режет `tools/build_starmap.py` хранилища PlanetX из файла EXR. Модуль
и Lite показывают карту в виде неба между Млечным путём и снимками DSS.
Данные NASA находятся в общественном достоянии, звёзды карты - Gaia DR2.
При показе указывается «NASA/Goddard SVS, Gaia DR2: ESA/Gaia/DPAC».

Folder `sky/starmap` holds the NASA SVS Deep Star Maps 2020 sky map
as HiPS tiles (JPEG 512×512, HEALPix orders 0-4). NASA data is in the
public domain, stars from Gaia DR2 (ESA/Gaia/DPAC).
