[![Github Downloads](https://img.shields.io/github/downloads/ERA-Projects/era-project-rus/total)](https://github.com/ERA-Projects/era-project-rus/releases)
[![ERA Discord Invite](https://img.shields.io/discord/665742159307341827?color=%237289DA&label=chat&logo=discord&logoColor=white)](https://discord.gg/bvfJGZe)

# ERA Project (Русская версия)
## Этот репозиторий используется для разработки и публикации релизов **Русской версии** ERA Projects.
> [!IMPORTANT]
> ### [ERA Project (English version) repository](https://github.com/ERA-Projects/era-project-eng)


# Установка игры
## 1. Автоматическая установка игры:
- Скачать [Heroes Launcher отсюда](https://github.com/HeroesLauncher/heroeslauncher/releases) и установить **НЕ** в системную папку;
- Выбрать вкладку "**ERA**" в списке игры;
- указать папку с любой рабочей версией игры "Heroes of Might and Magic III", основанной на "Shadow of Death", что может быть одним из:
    - Shadow of Death/SoD (Дыхание Смерти);
    - Complete (Полное Собрание) Купить можно в [UBISOFT Store](https://store.ubisoft.com/us/heroes-of-might-and-magic-3--complete/575ffd9ba3be1633568b4d8c.html), или в [GOG](https://www.gog.com/en/game/heroes_of_might_and_magic_3_complete_edition), или в [EPIC GAMES Store](https://store.epicgames.com/en-US/p/might-and-magic-heroes-3);
    - Master of Puppets/MOP;
    - In the Wake of Gods/WoG;
    - Horn of the Abyss/HotA (Рог Бездны) - Скачать можно с [Официального сайта](https://h3hota.com/ru/download);
- Выбрать необходимый язык установки сборки (Русский или Английский);
- Подтвердить или выбрать новую папку, куда будет установлена сборка;
- Дождаться скачивания и распаковки файлов;
- Нажать на кнопку "Шестерёнка" рядом с кнопкой "Играть"
- Выбрать пункт ``Настройки HD-мода``, чтобы запустить настройки HD Mod:
    - сменить язык на "Русский";
    - выставить желаемое разрешение игры;
    - рекомендуется режим ``(stretchable) 32-bit OpenGL by Verok``;
    - настроить ["**ТВИКИ**"](https://sites.google.com/site/heroes3hd/rus/%D1%82%D0%B2%D0%B8%D0%BA%D0%B8);
- Нажать "**Играть**" в Heroes Launcher, чтобы начать игру;

## 2. Ручная установка игры:
- Подготовить папку рабочей игры, основанной на любой рабочей версией игры "Heroes of Might and Magic III", основанной на "Shadow of Death", что может быть одним из:
    - Shadow of Death/SoD (Дыхание Смерти);
    - Complete (Полное Собрание) Купить можно в [UBISOFT Store](https://store.ubisoft.com/us/heroes-of-might-and-magic-3--complete/575ffd9ba3be1633568b4d8c.html), или в [GOG](https://www.gog.com/en/game/heroes_of_might_and_magic_3_complete_edition), или в [EPIC GAMES Store](https://store.epicgames.com/en-US/p/might-and-magic-heroes-3);
    - Master of Puppets/MOP;
    - In the Wake of Gods/WoG;
    - Horn of the Abyss/HotA (Рог Бездны) - Скачать можно с [Официального сайта](https://h3hota.com/ru/download);
- Создать папку, куда будут скопированы:
    - все ".dll" файлы из корневого каталога игры;
    - папка "MP3" - целиком
    - папка "Data" - с файлами:
      - "H3bitmap.lod";
      - "H3sprite.lod";
      - "Heroes3.snd";
      - "VIDEO.VID";
    - опционально папка "Maps", если нужны карты из неё, так как в Русской версии сборки есть переведённые все карты из "Полного Собрание";
- [**Скачать актуальный релиз**](https://github.com/ERA-Projects/era-project-rus/releases/latest) данного репозитория;
- Распаковать в подготовленную папку с игрой;
- Запустить файл ["Tools/install.bat"](Tools/install.bat) для инициализации списка модов по умолчанию или запустить ["Tools/Mod Manager/mmanager.cmd"](Tools/Mod%20Manager/mmanager.cmd) и подключить необходимые Моды (мод "WOG" обязателен);
- Запустить файл ["HD_Launcher.exe"](HD_Launcher.exe), чтобы запустить настройки HD Mod:
    - сменить язык на "Русский";
    - выставить желаемое разрешение игры;
    - рекомендуется режим ``(stretchable) 32-bit OpenGL by Verok``;
    - настроить ["**ТВИКИ**"](https://sites.google.com/site/heroes3hd/rus/%D1%82%D0%B2%D0%B8%D0%BA%D0%B8);
- Запустить файл ["h3era HD.exe"](h3era%20HD.exe), чтобы начать игру;

# Обновление игры
## 1. Автоматическое обновление игры:
- Запустить установленный ранее [Heroes Launcher](https://github.com/HeroesLauncher/heroeslauncher/releases)
- Нажать на кнопку "Шестерёнка" рядом с кнопкой "Играть";
- Выбрать пункт ``Проверить Обновления``;
- Дождаться завершения обновления;

## 2. Ручное обновление игры:
- [**Скачать актуальный релиз**](https://github.com/ERA-Projects/era-project-rus/releases/latest) данного репозитория;
- Убедиться, что между установленной версией и новой не было удалённых файлов в "Модах";
	- Если в каком-то моде такие файлы были, крайне рекомендуется удалить папку данного мода из папки с установленной игрой;
- Распаковать файлы из скачанного архива в папку с установленной игрой с заменой файлов, размер или дата которых отличаются;

# Удаление игры
## 1. Автоматическое удаление игры:
- Запустить установленный ранее [Heroes Launcher](https://github.com/HeroesLauncher/heroeslauncher/releases)
- Нажать на кнопку "Шестерёнка" рядом с кнопкой "Играть";
- Выбрать пункт ``Удалить``;
- *Опционально* можно Сохранить файлы базовой игры, удалив лишь файлы Игровой Сборки;
- Подтвердить удаление;

## 2. Ручное удаление игры:
- Удалить папку с игрой;

> [!NOTE]
> ## Чтобы получить последнюю версию проекта, загрузите ее с [РЕЛИЗОВ](https://github.com/ERA-Projects/era-project-rus/releases/latest)

> [!TIP]
> ## Для получения обновлений рекомендуется использовать [Heroes Launcher](https://github.com/HeroesLauncher/heroeslauncher/releases)
> ## [Список изменений](https://github.com/ERA-Projects/era-project-rus/blob/main/CHANGELOG.md)
> 
