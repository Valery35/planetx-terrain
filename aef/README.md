# AlphaEarth Foundations - указатель файлов по зонам UTM

Файл зоны (`40N.json` и т. д.) - квадраты 81 920 м набора AlphaEarth
Foundations Satellite Embedding: западный и северный край в метрах UTM
и имена файлов COG по годам 2017-2025 в виде «образ:строка:столбец»,
строка и столбец - в долях 8192 пикселей образа Earth Engine. Адрес
файла - `https://storage.googleapis.com/alphaearth_foundations/
satellite_embedding/v1/annual/<год>/<зона>/<образ>-<строка·8192>-
<столбец·8192>.tiff`.

Собран из `aef_index.parquet` Google сценарием
`tools/build_aef_index.py` модуля PlanetX 28 октября 2026 года.
Читает его `planetx/core/aef.py`.

Набор - CC BY 4.0. The AlphaEarth Foundations Satellite Embedding
dataset is produced by Google and Google DeepMind.
