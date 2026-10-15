# Server

Серверна частина збірки (modpack) проєкту **Gachiland** — Fabric-сервер із оптимізаціями продуктивності, генерацією світу (Terralith / Tectonic) та серверними інструментами адміністрування.

| Параметр | Значення |
|---|---|
| Версія Minecraft | `1.21.11` |
| Модлоадер | Fabric (`fabric-server-launch.jar`, `versions/1.21.11/server-1.21.11.jar`) |
| Fabric API | `0.141.6+1.21.11` |
| Кількість модів | 70 |
| Порт | `25565` |
| Слоти | `20` (MOTD: `GachiLand | Restart`) |
| Режим | виживання, складність `easy` |
| Авторизація | `online-mode=true` (лише ліцензійні акаунти) |
| White-list | `true` (наразі додано `Devayzer`) |
| Виділена пам'ять | `-Xms4096M -Xmx4096M` (Aikar's flags) |

---

## Моди

### Ядро та бібліотеки

- **Fabric API** — базове ядро для всіх Fabric-модів, обов'язкове на сервері.
- **Fabric Language Kotlin** — підтримка Kotlin для модів, написаних цією мовою.
- **Architectury API** — бібліотека для модів, сумісних з кількома лоадерами.
- **Balm** — бібліотека для модів Blay09.
- **GeckoLib** — бібліотека анімованих 3D-моделей (потрібна для `EnhancedCats`).
- **Framework** — спільна бібліотека для модів родини Framework.
- **JamLib** — допоміжна бібліотека для модів серії Jam.
- **mezz_config** — конфіг-бібліотека від автора JEI.
- **Placeholder API** — текстовий API з плейсхолдерами (використовується `TAB`).
- **PuzzlesLib** — бібліотека Fuzs для його модів.
- **ResourcefulLib** — бібліотека для модів серії Resourceful.
- **CreativeCore** — бібліотека для модів CreativeMD.
- **ForgeConfigAPIPort** — звичний Forge-формат конфігів на Fabric.
- **Polymer (bundled)** — серверний контент, що працює без встановлення мода на клієнті.
- **Lithostitched** — бібліотека генерації світу та датапаків (потрібна для `Terralith`).
- **Moogs Structure Library** — бібліотека структур для модів серії Moog's.
- **YetAnotherConfigLib (YACL)** — бібліотека конфіг-меню для сумісних модів.

### Оптимізація продуктивності

- **Lithium** — оптимізація ігрової логіки, фізики та ШІ мобів.
- **Krypton** — оптимізація мережевого стеку, знижує затримки.
- **FerriteCore** — суттєве зменшення споживання оперативної пам'яті.
- **C2ME** — паралельна генерація та завантаження чанків (alpha-версія).
- **Noisium** — оптимізація генерації світу (шум-функції worldgen).
- **ScalableLux** — масштабований рушій освітлення (швидша та паралельна обробка світла).
- **VMP (Very Many Players)** — оптимізація сервера під велику кількість одночасних гравців.
- **ServerCore** — набір серверних оптимізацій (моб-капи, динамічна продуктивність).
- **Ksyxis** — прискорення завантаження світу (без примусового прогріву спавн-чанків).
- **Clumps** — об'єднання XP-орбів у кластери, менше лагів.
- **Alternate Current** — оптимізація обробки редстоун-сигналів.
- **ThreadTweak** — кращий розподіл задач між потоками процесора.
- **Packet Fixer** — виправляє проблеми з розміром/обробкою мережевих пакетів.
- **Fast IP Ping** — швидший пінг сервера у списку серверів на клієнті.

### Світ, структури та генерація

- **Terralith** — масштабний оверхол біомів та рельєфу (`Terralith_1.21.11_v2.6.1_Fabric.jar`).
- **Tectonic** — нові форми рельєфу, гірські масиви та річкові системи.
- **Structory** — додаткові декоративні структури по всьому світу.
- **ChoiceTheorem's Overhauled Village (CTOV)** — перероблені та розширені села з урахуванням біомів.
- **DnT Pillager Outpost Overhaul** — покращені аутпости піліджерів.
- **HopoBetterMineshaft** — покращені шахти.
- **HopoBetterUnderwaterRuins** — покращені підводні руїни.
- **Moog's End Structures** — нові структури в Енді.
- **Moog's Nether Structures** — нові структури в Незері.
- **Moog's Voyager Structures** — структури для дослідження в усіх вимірах.
- **Nether Portal Fix** — коректна робота порталів у Незер (пари порталів не плутаються).

### Геймплей та контент

- **Better Combat** — нова бойова система: замах залежно від зброї, комбо, дальність удару.
- **Combat Roll** — перекат/ухиляння в бою.
- **Create** — механізми, автоматизація, кінетика (`create-fly-1.21.11-6.0.9-5.jar`).
- **Farmer's Delight** — фермерська кулінарія: нові культури, страви, ножі.
- **Brewery** — варіння напоїв, бочки, рецепти.
- **Friends & Foes** — нові моби (Copper Golem, Iceologer, Moobloom, Rascal, Glare).
- **Universal Graves** — могила з інвентарем на місці смерті (конфіг `config/universal-graves`).
- **Individual Keep Inventory** — збереження інвентаря з налаштуванням на кожного гравця окремо.
- **Refurbished Furniture** — меблі та предмети для декору.
- **Right Click Harvest** — збір врожаю правою кнопкою без повторної посадки.
- **Trade Cycling** — прокручування торгів селян без руйнування робочого блоку.
- **Simple Voice Chat** — проксиміті-голосовий чат (потрібен і на клієнті; налаштування у `config/voicechat`).
- **Female Gender Mod** — модель жіночого персонажа (синхронізація даних з клієнтом).
- **EnhancedCats** — кастомні моделі та анімації котів (GeckoLib).
- **Cat Fighting** — розширення боїв/взаємодії котів (мод збірки Gachiland).

### Адміністрування та серверні інструменти

- **EasyAuth** — серверна авторизація гравців; база даних `EasyAuth/easyauth.db`.
- **Chunky (Fabric)** — прогрів/пре-генерація чанків, менше лагів під час дослідження світу.
- **Chunky Offline** — прогрів світу без підключення гравців.
- **TAB** — табло, теги/префікси гравців, header/footer (конфіг `config/tab`).

### Клієнтські моди (є в папці `mods`, на сервері ефекту не дають)

- **Iris Shaders** — рендер шейдерів; суто клієнтський.
- **Sodium** — рендер-рушій; суто клієнтський.
- **Sodium Extra** — додаткові графічні налаштування; суто клієнтський.
- **Dark Loading Screen** — темний екран завантаження; суто клієнтський.
- **Mod Menu** — меню модів; суто клієнтський.
- **My Totem Doll** — модель тотема; суто клієнтський.
- **Player Animation Lib** — бібліотека анімацій моделі гравця; клієнтська.
- **Xaero's Minimap** — серверна підтримка синхронізації даних мапи.
- **Xaero's World Map** — серверна підтримка даних карти світу.

---

## Конфігурація сервера

Основні значення з `server.properties`:

| Параметр | Значення |
|---|---|
| `motd` | `GachiLand \| Restart` |
| `server-port` | `25565` |
| `max-players` | `20` |
| `view-distance` | `8` |
| `simulation-distance` | `6` |
| `difficulty` | `easy` |
| `gamemode` | `survival` |
| `online-mode` | `true` (ліцензійні акаунти) |
| `white-list` | `true` |
| `enforce-whitelist` | `false` |
| `enable-status` | `true` |
| `hide-online-players` | `false` |
| `spawn-protection` | `16` |
| `region-file-compression` | `lz4` |
| `network-compression-threshold` | `256` |
| `resource-pack` | `https://github.com/Devayzer/minecraft_mods/releases/download/Releases/logopack.zip` (не обов'язковий, `require-resource-pack=false`) |
| `level-name` | `world` (папка створюється під час першого запуску) |

Запуск (файл `run.sh`):

```sh
java -Xms4096M -Xmx4096M --add-modules=jdk.incubator.vector \
  -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 \
  -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch \
  -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 \
  -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 \
  -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1 \
  -Dusing.aikars.flags=https://mcflags.emc.gs -Daikars.new.flags=true \
  -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M \
  -XX:G1ReservePercent=20 -jar fabric-server-launch.jar --nogui
```

- Це стандартні **Aikar's flags** (G1GC) під 4 ГБ heap — запуск через `bash run.sh`.
- `fabric-server-launcher.properties` вказує `serverJar=server.jar`; сам Fabric-завантажувач — `fabric-server-launch.jar`, а версія гри лежить у `versions/1.21.11/`.
- `eula.txt` — `eula=true` (умови Mojang прийнято).
- Права: оператор `op-permission-level=4`, `ops.json` і `whitelist.json` — порожні зараз крім `Devayzer`.
- Авторизація: `EasyAuth` (SQLite-база `EasyAuth/easyauth.db`).
- `banned-ips.json` / `banned-players.json` — порожні списки банів.

## Примітки

- Конфіги модів лежать у `config/`, частина — у підпапках (`chunky`, `servercore`, `tab`, `voicechat`, `universal-graves`, `create` тощо).
- Версії модів мають відповідати клієнтським (Minecraft `1.21.11`, Fabric). Розбіжність версій може блокувати підключення або спричиняти десинк.
- `c2me`, `ScalableLux`, `VMP` — alpha/beta-версії: після оновлення гри їх варто оновлювати першими та тестувати окремо.
- Прогрів світу: `/chunky radius <блоки>` + `/chunky start` (або `chunky-offline` до першого запуску для гравців).
- Моб-капи та динамічну продуктивність налаштовує `servercore` (`config/servercore`).
- Голосовий чат `voicechat` відкриває власний UDP-порт (за замовчуванням `24454`) — має бути відкритий у фаєрволі/роутері.
- Клієнтські моди в папці `mods` сервера безпечні, але займають місце; за потреби їх можна видалити без впливу на роботу сервера.

## Файли модів (папка `mods`)

```text
alternate-current-mc1.21.11-1.9.0.jar
architectury-19.0.1-fabric.jar
balm-fabric-1.21.11-21.11.9.1.jar
bettercombat-fabric-3.1.0+1.21.11.jar
brewery-0.14.0+1.21.11-rc2.jar
c2me-fabric-mc1.21.11-0.4.0-alpha.0.28.jar
catfighting-fabric-1.21.11-1.2.1.jar
Chunky-Fabric-1.4.55.jar
chunky-offline-v1.1.0.jar
Clumps-fabric-1.21.11-29.0.0.1.jar
combat_roll-fabric-3.0.1+1.21.11.jar
create-fly-1.21.11-6.0.9-5.jar
CreativeCore_FABRIC_v2.14.11_mc1.21.11.jar
dark-loading-screen-1.6.17.jar
DnT-pillager-outpost-overhaul-v3.3 [Fabric].jar
easyauth-mc1.21.11-3.4.4.jar
EnhancedCats-1.21.11-1.2.jar
fabric-api-0.141.6+1.21.11.jar
fabric-language-kotlin-1.14.1+kotlin.2.4.20.jar
FarmersDelight-1.21.11-3.6.16+refabricated.jar
fast-ip-ping-v1.0.12-mc1.21.11-fabric.jar
Female-Gender-Mod-fabric-5.0.0-Beta.3+1.21.11.jar
ferritecore-8.2.0-fabric.jar
ForgeConfigAPIPort-v21.11.1-mc1.21.11-Fabric.jar
framework-fabric-1.21.11-0.13.10.jar
friendsandfoes-fabric-5.0.2+mc1.21.11.jar
geckolib-fabric-1.21.11-5.4.5.jar
graves-3.10.2+1.21.11.jar
HopoBetterMineshaft-[1.21.11]-1.3.5.jar
HopoBetterUnderwaterRuins-[1.21.11]-1.2.6.jar
individualkeepinv-1.0.0.jar
iris-fabric-1.10.8+mc1.21.11.jar
jamlib-fabric-2.0.0+1.21.11.jar
krypton-0.2.10.jar
Ksyxis-1.4.6.jar
lithium-fabric-0.21.4+mc1.21.11.jar
lithostitched-1.7.2-fabric-21.11.jar
mezz_config-1.21.11-fabric-0.6.8.jar
modmenu-17.0.1.jar
MoogsEndStructures-universal-1.21-2.1.1.jar
MoogsNetherStructures-universal-1.21-3.1.1.jar
MoogsStructureLib-fabric-1.21.11-3.4.2.jar
MoogsVoyagerStructures-universal-1.21-5.1.3.jar
MyTotemDoll-2.3.3+1.21.11.jar
netherportalfix-fabric-1.21.11-21.11.3.jar
noisium-fabric-2.8.3+mc1.21.11.jar
packetfixer-fabric-3.3.5-1.21.11.jar
placeholder-api-2.8.2+1.21.10.jar
PlayerAnimationLibFabric-1.1.11+mc.1.21.11.jar
polymer-bundled-0.15.2+1.21.11.jar
PuzzlesLib-v21.11.13-mc1.21.11-Fabric.jar
refurbished_furniture-fabric-1.21.11-1.0.22.jar
ResourcefulLib-fabric-1.21.11-3.11.1.jar
rightclickharvest-fabric-4.6.1+1.21.11.jar
ScalableLux-fabric-0.3.0-alpha.0.3-all.jar
servercore-fabric-1.5.15+1.21.11.jar
sodium-extra-fabric-0.9.4+mc1.21.11.jar
sodium-fabric-0.8.15-beta.1+mc1.21.11.jar
Structory_26.2_v1.3.7.jar
TAB v6.0.1.jar
tectonic-3.0.19-fabric-1.21.11.jar
Terralith_1.21.11_v2.6.1_Fabric.jar
threadtweak-fabric-0.1.8+mc1.21.11.jar
trade-cycling-fabric-1.21.11-1.0.22.jar
vmp-fabric-mc1.21.11-0.2.0+beta.7.227-all.jar
voicechat-fabric-1.21.11-2.6.24.jar
xaerominimap-fabric-1.21.11-26.6.0.jar
xaeroworldmap-fabric-1.21.11-1.47.0.jar
yet_another_config_lib_v3-3.8.2+1.21.11-fabric.jar
[fabric]ctov-1.21.11-3.6.2a.jar
```
