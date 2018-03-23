## sAutoSetting

### Пакет для автоматизации действий после установки MODX.

## ВНИМАНИЕ! Для установки на чистый MODX!

### Системные настройки, которые будут изменены:

#### Раздел «Словарь и язык»

* «Локаль» — ru_RU.utf-8 (locale)
* «Язык» — ru (cultureKey)
* «Язык текстового редактора во фронтенде сайта» — ru (fe_editor_lang)
* «Язык панели управления» — ru (manager_language)
* «Языковые атрибуты HTML и XML панели управления» — ru (manager_lang_attribute)

#### Раздел «Дружественные URL»

* «Суффикс контейнера» — Пусто (container_suffix)
* «Создавать ЧПУ-псевдоним (так называемые «дружественные URL») «на лету»» — Да (friendly_alias_realtime)
* «Метод фильтрации символов в псевдонимах» — alphanumeric (friendly_alias_restrict_chars)
* «Транслитерация псевдонимов» — russian_yandex (friendly_alias_translit)
* «Использовать дружественные URL» — Да (friendly_urls)
* «Строгий режим дружественных URL» — Да (friendly_urls_strict)
* «Использовать вложенные URL» — Да (use_alias_path)

#### Раздел «Сайт»

* «Публиковать по умолчанию» — Да (publish_default)
* «Схема URL» — abs (link_tag_scheme)

#### Раздел «Панель управления»

* «Показывать описание в верхнем меню» — Нет (topmenu_show_descriptions)

#### Раздел «Файловая система»

* «Максимальный размер загрузки» — 10485760 (upload_maxsize)

#### Раздел «Шлюз»

* «Строгий метод запроса» — Да (request_method_strict)
* Типы содержимого (убираем .html у ресурсов).

Будет создана категория «SEO», в которой будут созданы:

* TV «seo_h1» — Заголовок h1
* TV «seo_description» — meta description
* TV «seo_keywords» — meta keywords
* TV «seo_index» — Индексировать страницу (чекбокс, по умолчанию включен)
* Snippet «Canonical» — заменям base href

«Начальный шаблон» будет переименован в «Главная страница», немного заменено содержимое, создан шаблон «Вторичная страница», а так же подключены все 4 TV параметра.

#### Автоматически будут созданы 3 документа:

* Ошибка 404 (шаблон «Текстовая страница») — он же и пропишется в системные настройки
* sitemap.xml (пустой шаблон) — карта сайта, в содержимом сразу будет вызов pdoSitemap
* robots.txt (пустой шаблон) — правила robots.txt для MODX Revolution, найденные на просторах интернета

Перед установкой, вам будет доступно выбрать пакеты, которые автоматически установятся:

* Ace
* autoRedirector
* ClientConfig
* FormIt
* MIGX
* MinifyX
* modLastModified
* pdoTools
* phpThumbOn

Пакет «translit» установится в любом случае, независимо от всех остальных опций (в системных настройках уже будет стоять автоматическая транслитерация URL). Так же копируется новая таблица транслитизации по правилам яндекса.