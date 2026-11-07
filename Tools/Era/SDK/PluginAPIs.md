# API плагинов ERA Project 2.300

Собирайте нативные плагины для **Win32 (x86)** с C++17. Добавьте `Tools/Era/SDK` в пути поиска заголовков.

- `EraPluginsAPI/ErmFunctionsAPI.h` объявляет типы экспортов Runtime Services для `GetProcAddress`. ERM-скрипты вызывают те же экспорты напрямую через `SN:F`.
- `EraPluginsAPI/GraphicsAPI.h`, `ConfigExportAPI.h` и `ConfigExportUIAPI.h` предоставляют работу с кадрами DEF в памяти, регистрацию провайдеров конфигурации и открытие диалога экспорта.
- `EraPluginsAPI/ObjectDefinitionsAPI.h`, `ObjectExtenderAPI.hpp` и `ObjectDataAPI.h` предоставляют объединённый каталог объектов, обработчики и лимиты ГСК, а также данные жилищ. Корневой `ObjectExtenderAPI.hpp` подключает актуальный заголовок. Сохраняйте папки `Objects/` и `Era/` рядом с `EraPluginsAPI/`, чтобы работали относительные пути.
- `EraPluginsAPI/TextOverridesAPI.h` и `WogificationAPI.h` предоставляют привязки текстов и правила вогификации из скриптов. Перед перемещением или освобождением ячеек с текстом снимайте привязки через `forget`. Отдельный диалог настроек вогификации в этой сборке отключён.
- `MainMenuAPI.hpp`, `SystemOptionsAPI.h` и `ArtifactDescriptionApi.h` доступны по прежним путям. Для отдельного плагина справки используйте [HelpDialogAPI.hpp из репозитория исходников](https://github.com/daemon1995/h3era_plugins/blob/63b169c6cf44e0c29088dfa2ac98659a85700baf/headers/EraPluginsAPI/HelpDialogAPI.hpp).

Перед заголовками, которые подключают `RuntimeServices.h`, подключите Patcher API. Входящий в SDK H3API содержит этот интерфейс и нативные структуры для API объектов. Определите `_H3API_PATCHER_X86_` до первого подключения H3API. Если в проекте уже есть совместимый H3API с включённым Patcher, используйте его.

```cpp
#define _H3API_PATCHER_X86_
#include "H3API/H3API.hpp"
#include "EraPluginsAPI/GraphicsAPI.h"
#include "EraPluginsAPI/ConfigExportAPI.h"
#include "ObjectExtenderAPI.hpp"

bool GraphicsReady()
{
    const auto* api = era_graphics::GetApi();
    return api && api->isReady();
}
```

Получайте таблицы сервисов в игровом потоке. Совместимая таблица может появиться позже при запуске. Для графики можно подписаться на `OnGraphicsResourcesReady`, а для провайдеров экспорта — на `OnConfigExportApiReady`. Регистрируйте расширители ГСК до завершения загрузки определений объектов.
