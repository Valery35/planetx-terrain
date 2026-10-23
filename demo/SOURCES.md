# Демо PlanetX - источники и условия

Сцены демо `*.planetx` и файлы в папках `brienz`, `haul`, `quarry`,
`subsurface`, `vegas` собраны ООО «Информ++» скриптами `tools/make_*.py`
хранилища [PlanetX](https://github.com/Valery35/planetx). Сцены
и файлы, кроме перечисленных ниже чужих данных, распространяются
по лицензии GNU GPL версии 3, текст - `LICENSE` рядом.

Демо открывают модуль QGIS PlanetX и программа PlanetX Lite. Файлы
берутся по адресу
`https://raw.githubusercontent.com/Valery35/planetx-terrain/main/demo/<путь>`.

Чужие данные в файлах демо сохраняют свои условия:

| Файлы | Источник | Условия | Подпись |
|---|---|---|---|
| `models.planetx` | 3D-модели Valery35, 3D Warehouse - Зачатьевская церковь в Суздале и церковь Покрова Пресвятой Богородицы в Перми | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | Valery35, 3D Warehouse, CC BY 4.0 |
| `brienz/brienzersee_bed.tif` | swissBATHY3D, swisstopo, отметки дна Бриенцского озера 10 м из сеток 1 м | [открытые данные swisstopo](https://opendata.swiss/en/dataset/swissbathy3d-bathymetrische-daten-von-schweizer-seen), указание источника обязательно | swisstopo swissBATHY3D |
| `quarry/quarry_dem.tif` | высоты Mapzen Terrain Tiles, карьер и отвал выдуманы | [условия Terrain Tiles](https://github.com/tilezen/joerd/blob/master/docs/attribution.md) | Terrain: Mapzen, SRTM, GMTED, ETOPO1 and others |
| `vegas/vegas_loop.gpkg`, `vegas/stations.json` | OpenStreetMap, тоннели The Boring Company и станции, один запрос Overpass | [ODbL](https://www.openstreetmap.org/copyright), файлы - производная база данных под ODbL | © OpenStreetMap contributors |
| `haul/*` | съезды карьеров сняты по снимку Esri World Imagery, рельеф - Copernicus DEM GLO-30, самосвал условный | Copernicus DEM - [лицензия ESA](https://dataspace.copernicus.eu/explore-data/data-collections/copernicus-contributing-missions/collections-description/COP-DEM) | produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH 2014-2018 provided under COPERNICUS by the European Union and ESA |
| `subsurface/*` | скважины и кровли у Березников синтетические | GNU GPL 3, как сцены | - |
| `aral.planetx` | ссылки на снимки NASA GIBS MODIS Terra и файлы Wikimedia Commons «Moynaq, Aral Lake, Ship Wrecks, Uzbekistan.jpg» (THORSTEN, CC BY-SA 4.0) и «Aral map.png» (Kmusser, CC BY-SA 2.5) | в сцене лежат ссылки, картинки не хранятся | NASA GIBS, авторы файлов Commons в описаниях |
| `moscow.planetx` | сцена включает карты Москвы 1813-1935 годов с Wikimedia Commons, привязка Wikimaps Warper | общественное достояние, тайлы не хранятся | Wikimedia Commons, Wikimaps Warper |
| `trains.planetx` | сцена включает положения поездов Fintraffic Digitraffic | [CC BY 4.0](https://www.digitraffic.fi/en/railway-traffic/), данные не хранятся | Fintraffic / digitraffic.fi |
| `superoverlay.planetx` | ссылка на образец суперналожения KML Google, Маунтин-Вью | файл образца не хранится | - |

Подробный перечень источников модуля - `doc/SOURCES.md` хранилища
PlanetX.

---

PlanetX demo scenes and files by Inform++ LLC, GNU GPL 3 (`LICENSE`).
Third-party data keep their terms: models - Valery35, CC BY 4.0,
Brienz lake bed - swisstopo swissBATHY3D, Vegas Loop - © OpenStreetMap
contributors, ODbL, haul relief - Copernicus DEM GLO-30, quarry relief -
Mapzen Terrain Tiles. Scenes `aral`, `moscow`, `trains` and
`superoverlay` hold links only, see the table above.
