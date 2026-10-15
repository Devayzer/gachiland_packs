# Client

Клієнтська збірка (modpack) проєкту **Gachiland** — оптимізований Fabric-клієнт з графічними покращеннями, анімаціями мобів та зручним інтерфейсом.

| Параметр | Значення |
|---|---|
| Версія Minecraft | `1.21.11` |
| Модлоадер | Fabric |
| Fabric API | `0.141.6+1.21.11` |
| Fabric Language Kotlin | `1.14.1+kotlin.2.4.20` |
| Кількість модів | 70 |
| Ресурспаків у папці | 5 + 1 папка (`EnhancedCats`) |
| Шейдерпаків | 1 (`BSL_v10.1.8`) |

---

## Моди

### Ядро та бібліотеки

- **Fabric API** — базове ядро для всіх Fabric-модів, без нього більшість модів не запуститься.
- **Fabric Language Kotlin** — підтримка Kotlin для модів, написаних цією мовою.
- **Architectury API** — бібліотека для модів, що працюють і на Fabric, і на Forge/NeoForge.
- **Cloth Config API** — стандартна бібліотека конфігураційних GUI.
- **YetAnotherConfigLib (YACL)** — сучасна бібліотека конфіг-меню (використовується багатьма модами).
- **Balm** — бібліотека для модів Blay09 (меблі, крафт-утиліти тощо).
- **GeckoLib** — бібліотека анімованих 3D-моделей (потрібна для `EnhancedCats`).
- **Framework** — спільна бібліотека для модів родини Framework.
- **JamLib** — допоміжна бібліотека (використовується модами серії Jam).
- **Placeholder API** — текстовий API з підстановкою плейсхолдерів.
- **mezz_config** — конфіг-бібліотека від автора JEI.
- **PuzzlesLib** — бібліотека Fuzs для його модів.
- **ResourcefulLib** — бібліотека для модів Resourceful Bees/серії Resourceful.
- **CreativeCore** — бібліотека для модів CreativeMD (зокрема `AmbientSounds`).
- **ForgeConfigAPIPort** — дозволяє модам використовувати звичний Forge-формат конфігів на Fabric.
- **Polymer (bundled)** — бібліотека для серверного контенту, що працює без встановлення мода на клієнті.
- **Lithostitched** — бібліотека для генерації світу та датапаків.

### Оптимізація та продуктивність

- **Sodium** — повна заміна рендер-рушія, основне джерело приросту FPS.
- **Sodium Extra** — додаткові графічні налаштування до Sodium (частинки, туман, погода).
- **Lithium** — оптимізація ігрової логіки, фізики та штучного інтелекту мобів.
- **Krypton** — оптимізація мережевого стеку, знижує затримки на серверах.
- **FerriteCore** — суттєве зменшення споживання оперативної пам'яті.
- **ImmediatelyFast** — прискорення рендеру інтерфейсу, карт та текстур мобів.
- **Entity Culling** — не рендерить ентитети, які не видно (за стінами / поза камерою).
- **More Culling** — розширене відсікання блоків, листя, скринь тощо.
- **BadOptimizations** — набір дрібних мікрооптимізацій рендеру та логіки.
- **Dynamic FPS** — знижує FPS, коли гра у фоні (економія ресурсів ПК).
- **ThreadTweak** — покращений розподіл задач між потоками процесора.
- **Packet Fixer** — виправляє проблеми з розміром/обробкою мережевих пакетів.
- **Fast IP Ping** — значно швидший пінг серверів у списку серверів.
- **FPS Display** — показ FPS та часу кадру на екрані.

### Графіка, анімації та візуал

- **Iris Shaders** — підтримка шейдерпаків (аналог OptiFine Shaders на Fabric).
- **Continuity** — з'єднані текстури (CTM) для блоків.
- **Better Clouds** — якісніші та об'ємніші хмари.
- **Particle Rain** — покращений дощ, сніг та інші погодні частинки.
- **Particular** — набір клієнтських частинок (падаюче листя, бризки, пил тощо).
- **LambDynamicLights** — динамічне освітлення від предметів у руці та ентитетів.
- **Not Enough Animations** — анімації від першої особи (руки, їжа, мапи).
- **Entity Model Features (EMF)** — підтримка кастомних моделей ентитетів з ресурспаків (потрібна для `Fresh Animations`).
- **Entity Texture Features (ETF)** — кастомні текстури ентитетів, емісивні та анімовані очі.
- **Skin Layers 3D** — об'ємні шари скіна (куртка, капелюх, рукави).
- **Wavy Capes** — хвилястий плащ замість «пластикового».
- **Player Animation Lib** — бібліотека кастомних анімацій моделі гравця.
- **My Totem Doll** — тотем у руці/на персонажі з окремою моделлю та налаштуваннями.
- **Dark Loading Screen** — темний екран завантаження замість стандартного.
- **EnhancedCats** — кастомні моделі та анімації котів (GeckoLib); моделі додаються через ресурспак `EnhancedCats`.

### Геймплей та контент

- **Better Combat** — нова бойова система: замах залежно від зброї, комбо, дальність удару.
- **Combat Roll** — перекат/ухиляння в бою.
- **Create** — механізми, автоматизація, кінетика (`create-fly-1.21.11-6.0.9-5.jar`, конфіги `flywheel-client.json`, `ponder-client.json`).
- **Farmer's Delight** — фермерська кулінарія: нові культури, страви, ножі.
- **Brewery** — варіння напоїв, бочки, рецепти алкоголю/напоїв.
- **Friends & Foes** — нові моби (Copper Golem, Iceologer, Moobloom, Rascal, Glare).
- **Graves** — могила з інвентарем на місці смерті замість втрати речей.
- **AmbientSounds** — атмосферні звуки навколишнього середовища (печери, ліс, вітер).
- **Simple Voice Chat** — голосовий чат у грі (потрібен і на сервері).
- **Female Gender Mod** — модель жіночого персонажа з окремими налаштуваннями.
- **Refurbished Furniture** — меблі та предмети для декору будинку.
- **Right Click Harvest** — збір врожаю правою кнопкою без повторної посадки.
- **Trade Cycling** — прокручування торгів селян без руйнування робочого блоку.
- **Cat Fighting** — розширення боїв/взаємодії котів (мод збірки Gachiland).

### Інтерфейс та зручність

- **JEI (Just Enough Items)** — перегляд рецептів та використання предметів.
- **Mod Menu** — меню встановлених модів з переходами в їхні конфіги.
- **Xaero's Minimap** — мінімапа з точками та гравцями.
- **Xaero's World Map** — повна карта світу (шукач, маршрути, вайпоінти).
- **AppleSkin** — інформація про насичення, голод та ефекти їжі.
- **Mouse Tweaks** — зручне перетягування предметів у інвентарі.
- **Nemo's Inventory Sorting** — швидке сортування інвентарю та скринь.
- **ShulkerBoxTooltip** — перегляд вмісту шалкера/бочки у тултіпі.
- **Smooth Swapping** — плавна анімація переміщення предметів між слотами.
- **Ok Zoomer** — наближення (zoom) з налаштуванням чутливості та плавності.

---

## Ресурспаки (`resourcepacks/`)

| Ресурспак | Призначення | Статус |
|---|---|---|
| `FA+All_Extensions-v1.8.1.zip` | Офіційні розширення до Fresh Animations | увімкнено |
| `FreshAnimations_v1.10.4.zip` | Нові анімації всіх мобів (потрібні EMF + ETF) | увімкнено |
| `+1.21.3 Fresh Moves v3.1.1 (With Animated Eyes).zip` | Плавніші рухи мобів + анімовані очі | увімкнено |
| `Enhanced Audio r7.zip` | Покращені та детальніші звуки | лежить у папці, не увімкнено |
| `logopack.zip` | Кастомний логотип/меню | лежить у папці, не увімкнено |
| `EnhancedCats/` (папка в корені клієнта) | Кастомні моделі й текстури котів (`.geo.json` + `.png`) | підключається як ресурспак вручну |

- Порядок увімкнення важливий: спочатку `FA+All_Extensions`, далі `FreshAnimations`, і зверху `Fresh Moves`.
- `Fresh Moves` позначений як несумісний у `options.txt` — це нормально, він працює завдяки EMF/ETF.
- Як додавати власні моделі котів — див. `EnhancedCats/README.txt`.

## Шейдери (`shaderpacks/`)

| Шейдерпак | Призначення | Статус |
|---|---|---|
| `BSL_v10.1.8.zip` | BSL Shaders — м'яке освітлення, тіні, кольорокорекція | у папці, у налаштуваннях не вибраний |

- Рендер шейдерів виконує мод **Iris**; у `config/iris.properties` шейдери увімкнені (`enableShaders=true`), але активний пак не вибраний (`shaderPack=`) — виберіть BSL у меню шейдерів (стандартна клавіша **O**).
- Для коректних тіней рекомендовано `maxShadowRenderDistance=32` (значення за замовчуванням у цьому конфігу).

## Примітки

- Ресурспаки перезавантажуються комбінацією **F3 + T**, шейдери — через меню Iris.
- Конфіги модів лежать у `config/`, окремі налаштування — у `config/<назва моду>`.
- Голосовий чат (`voicechat`) працює лише там, де мод встановлено і на сервері.
- `datapacks/` та `data/` призначені для контенту, який не потребує модів на клієнті (Polymer).

## Файли модів (папка `mods`)

```text
AmbientSounds_FABRIC_v6.3.5_mc1.21.11.jar
appleskin-fabric-mc1.21.11-3.0.8.jar
architectury-19.0.1-fabric.jar
BadOptimizations-2.4.1-1.21.11.jar
balm-fabric-1.21.11-21.11.9.1.jar
better-clouds-1.13.11+1.21.11-fabric.jar
bettercombat-fabric-3.1.0+1.21.11.jar
brewery-0.14.0+1.21.11-rc2.jar
catfighting-fabric-1.21.11-1.2.1.jar
cloth-config-21.11.153-fabric.jar
combat_roll-fabric-3.0.1+1.21.11.jar
continuity-3.0.1-beta.1+1.21.11.jar
create-fly-1.21.11-6.0.9-5.jar
CreativeCore_FABRIC_v2.14.11_mc1.21.11.jar
dark-loading-screen-1.6.17.jar
dynamic-fps-3.11.6+minecraft-1.21.11-fabric.jar
EnhancedCats-1.21.11-1.2.jar
entityculling-fabric-1.11.3-mc1.21.11.jar
entity_model_features-3.3.11-1.21.11-fabric.jar
entity_texture_features-7.2.5-1.21.11-fabric.jar
fabric-api-0.141.6+1.21.11.jar
fabric-language-kotlin-1.14.1+kotlin.2.4.20.jar
FarmersDelight-1.21.11-3.6.16+refabricated.jar
fast-ip-ping-v1.0.12-mc1.21.11-fabric.jar
Female-Gender-Mod-fabric-5.0.0-Beta.3+1.21.11.jar
ferritecore-8.2.0-fabric.jar
ForgeConfigAPIPort-v21.11.1-mc1.21.11-Fabric.jar
fpsdisplay-4.5.1+1.21.11.jar
framework-fabric-1.21.11-0.13.10.jar
friendsandfoes-fabric-5.0.2+mc1.21.11.jar
geckolib-fabric-1.21.11-5.4.5.jar
graves-3.10.2+1.21.11.jar
ImmediatelyFast-Fabric-1.14.3+1.21.11.jar
iris-fabric-1.10.8+mc1.21.11.jar
jamlib-fabric-2.0.0+1.21.11.jar
jei-1.21.11-fabric-27.44.0.105.jar
krypton-0.2.10.jar
lambdynamiclights-4.9.1+1.21.11.jar
lithium-fabric-0.21.4+mc1.21.11.jar
lithostitched-1.7.2-fabric-21.11.jar
mezz_config-1.21.11-fabric-0.6.8.jar
modmenu-17.0.1.jar
moreculling-fabric-1.21.11-1.6.2.jar
MouseTweaks-fabric-mc1.21.11-2.30.jar
MyTotemDoll-2.3.3+1.21.11.jar
nemos-inventory-sorting-Fabric-1.21.11-1.14.9.jar
notenoughanimations-fabric-1.12.6-mc1.21.11.jar
ok_zoomer-fabric-16.0.0-beta.2.jar
packetfixer-fabric-3.3.5-1.21.11.jar
particlerain-4.0.2+1.21.11-fabric.jar
particular-1.21.11-Fabric-1.3.2.jar
placeholder-api-2.8.2+1.21.10.jar
PlayerAnimationLibFabric-1.1.11+mc.1.21.11.jar
polymer-bundled-0.15.2+1.21.11.jar
PuzzlesLib-v21.11.13-mc1.21.11-Fabric.jar
refurbished_furniture-fabric-1.21.11-1.0.22.jar
ResourcefulLib-fabric-1.21.11-3.11.1.jar
rightclickharvest-fabric-4.6.1+1.21.11.jar
shulkerboxtooltip-fabric-5.2.14+1.21.11.jar
skinlayers3d-fabric-1.11.3-mc1.21.11.jar
smoothswapping-0.9.8-1.21.11-fabric.jar
sodium-extra-fabric-0.9.4+mc1.21.11.jar
sodium-fabric-0.8.15-beta.1+mc1.21.11.jar
threadtweak-fabric-0.1.8+mc1.21.11.jar
trade-cycling-fabric-1.21.11-1.0.22.jar
voicechat-fabric-1.21.11-2.6.24.jar
waveycapes-fabric-1.11.2-mc1.21.11.jar
xaerominimap-fabric-1.21.11-26.6.0.jar
xaeroworldmap-fabric-1.21.11-1.47.0.jar
yet_another_config_lib_v3-3.8.2+1.21.11-fabric.jar
```
