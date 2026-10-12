# ЛР 2. Аналіз алгоритмізовності. Здобування знань

## 1. Формалізація задачі

r_A = f(q, S₁) — алгоритмічний підхід; r_D = g(q, S₁, S₂, Z) — декларативний.

| Компонент | Зміст |
|---|---|
| q | Підтримувати температуру, відносну вологість і концентрацію CO₂ у теплиці з томатами в межах норми для поточної фази розвитку з мінімальними витратами енергії. |
| S₁ | 1) показання датчиків температури повітря; 2) відносна вологість; 3) концентрація CO₂; 4) освітленість (сонячна радіація); 5) температура надворі; 6) час доби; 7) поточний стан кватирок, обігріву, екрана; 8) фаза розвитку культури за календарем. |
| S₂ | 1) раптова зміна хмарності та сонячної радіації; 2) сильний вітер або дощ, коли кватирки відкривати не можна; 3) різке нічне похолодання або заморозок; 4) відмова датчика (хибні показання) або виконавчого механізму; 5) конденсат на листі й початок хвороби (сіра гниль); 6) нерівномірний розвиток рослин у різних частинах теплиці; 7) відчинені двері, полив та інші дії працівників; 8) зміна ціни енергії. |
| Z | 1) норми температури вдень і вночі для томата за фазами; 2) пороги ризику хвороб (вологість, тривалість зволоження листя); 3) вплив вентиляції одночасно на температуру, вологість і CO₂; 4) теплова інерція теплиці та правило поступової зміни температури; 5) умови, за яких подача CO₂ має сенс (день, закриті кватирки); 6) вплив температури й вологості на запилення та зав’язування плодів; 7) способи зниження вологості без провітрювання (циркуляція повітря). |

## 2. Джерела квазіалгоритмічності

| Джерело | Бал (0–3) | Прояв у задачі |
|---|---|---|
| Випадкові чинники | 3 | Погода, хмарність і сонячна радіація змінюються протягом години й визначають, яка дія правильна; можливі відмови датчиків. |
| Особливості виконавця | 1 | Різні джерела й агрономи використовують різні уставки (С4, С5), але після їх фіксації правило розуміється однозначно. |
| Нечіткість формулювань | 2 | У джерелах трапляються «надмірна освітленість», «висока вологість», «надворі холодно», «швидко підвищувати» без чисел. |
| «Свобода волі» | 2 | Для однієї ситуації допустимі кілька дій: провітрювання, обігрів із провітрюванням або лише циркуляція повітря. |

Переважне джерело — **випадкові чинники**; основний апарат — ймовірнісні моделі, додатковий — нечітка логіка (ЛР 11).

## 3. Питання інтерв'ю

| № | Тип | Питання |
|---|---|---|
| 1 | загальне | Які типові ситуації з мікрокліматом трапляються в теплиці з томатами протягом доби? |
| 2 | порядок дій | З чого ви починаєте, коли зранку в теплиці висока вологість? |
| 3 | порядок дій | У якій послідовності вмикаєте вентиляцію, затінення й охолодження, коли теплиця перегрівається? |
| 4 | порядок дій | Що робите першим, коли вночі температура падає нижче норми? |
| 5 | загальне | На які показники дивитеся в першу чергу, вирішуючи, чи подавати CO₂? |
| 6 | винятки | Коли правило «жарко — охолоди» не спрацьовує або шкодить? |
| 7 | винятки | Чи бувають ситуації, коли вологість висока, а провітрювати не можна? Що тоді? |
| 8 | винятки | Коли не можна різко змінювати температуру, навіть якщо вона поза нормою? |
| 9 | помилки | Які типові помилки робить новачок у керуванні мікрокліматом? |
| 10 | помилки | Через які кліматичні помилки найчастіше втрачається врожай? |
| 11 | загальне | Що змусило б вас змінити режим, який зазвичай працює? |
| 12 | помилки | Чого не знає новачок про зв’язок між вологістю та хворобами? |

## 4. Протокол сеансу

- Дата: 12.10.2026
- Спосіб: аналіз джерел
- Тривалість: ≈ 60 хв

| Код | Документ | Посилання |
|---|---|---|
| Д1 | How to Grow Greenhouse Crops, Ch. 3 (Tomatoes). University of Arizona, Controlled Environment Agriculture Center (CEAC). | https://ceac.arizona.edu/sites/default/files/Ch3.pdf |
| Д2 | Pundt L. Botrytis blight on Greenhouse Crops. UConn Extension, Integrated Pest Management Program, 2012 (ред. 2023). | https://ipm.cahnr.uconn.edu/wp-content/uploads/sites/3216/2023/12/2023botrytisblightfactsheetfinal.pdf |
| Д3 | Trinklein D. Understanding Tomato Fruit Set. University of Missouri, Integrated Pest Management, 01.04.2013. | https://ipm.missouri.edu/mpg/2013/4/Understanding-Tomato-Fruit-Set |
| Д4 | Controlling High Tunnel Environment: Managing Temperature. USDA Natural Resources Conservation Service (NRCS), 2014. | https://www.nrcs.usda.gov/sites/default/files/2022-10/Controlling-High-Tunnel-Environment.pdf |
| Д5 | Botacchi A. C. CO₂ and You. North Carolina State University Extension (HortScans). | https://hortscans.ces.ncsu.edu/file/../uploads/c/o/co2_and__53b43cb48ce99.pdf |

| Пит. | Джерело | Дослівне формулювання | Переклад |
|---|---|---|---|
| 1 | Д1 | Production temps = 20-25 C (68-77 F) day / 15-17C (60-64 F) night. | Температура у фазі продукції — 20–25 °C вдень / 15–17 °C вночі. |
| 1 | Д1 | Day temps should be higher than night temps. | Денна температура має бути вищою за нічну. |
| 2 | Д2 | In greenhouses with vents, turn the heat on and crack the vents open about one inch. | У теплицях з кватирками ввімкніть обігрів і привідкрийте кватирки приблизно на дюйм. |
| 2 | Д2 | Heat and vent two or three times per hour in the evening after the sun goes down and early in the morning at sunrise. | Нагрівайте й провітрюйте два-три рази на годину ввечері після заходу сонця та рано вранці на світанку. |
| 2 | Д2 | The cooler, outside air will lower humidity levels as it is warmed in the greenhouse. | Прохолодніше зовнішнє повітря знижує вологість, коли нагрівається в теплиці. |
| 3 | Д1 | Adequate cooling: Either passive (vents or shade), active (fan and pad), or both. | Достатнє охолодження: пасивне (кватирки або затінення), активне (вентилятор і зволожувальна панель) або обидва. |
| 3 | Д1 | If light is too high (causing sunscald or plant stress) shading may be needed. | Якщо світла забагато (опіки чи стрес рослин), може знадобитися затінення. |
| 3 | Д4 | tomatoes grow best at 70 to 75°F and have a maximum air temperature of 85°F. | Томати найкраще ростуть за 21–24 °C, максимальна температура повітря — 29 °C. |
| 4 | Д1 | If possible, “ramp” temp up from ~3am to dawn | За можливості поступово піднімайте температуру з ~3:00 до світанку. |
| 4 | Д3 | Conversely, nighttime temperatures below 55 degrees F also promotes blossom drop. | І навпаки, нічна температура нижче 13 °C також спричиняє опадання квіток. |
| 5 | Д5 | Normally a 1000-1500 ppm carbon dioxide level is maintained in a closed greenhouse during the daylight hours. | Зазвичай у закритій теплиці в світлий час доби підтримують 1000–1500 ppm CO₂. |
| 5 | Д1 | You can enrich in the greenhouse up to 800 - 1000 ppm, but this costs money $$! | Можна збагачувати повітря до 800–1000 ppm, але це коштує грошей. |
| 5 | Д1 | Carbon dioxide generation: This is especially important for Winter mornings. | Подача CO₂ особливо важлива зимовими ранками. |
| 5 | Д5 | assuming that water, fertility, temperature, and light are at the optimum levels. | …за умови, що вода, живлення, температура й світло на оптимальному рівні. |
| 6 | Д1 | On hot, humid days, fan and pad cooling adds moisture but does not cool as well. | У спекотні вологі дні випарне охолодження додає вологу, але гірше охолоджує. |
| 6 | Д1 | The sun rises, but it’s cold. So if fans come on, it’s only for a short time. | Сонце сходить, але холодно. Тож якщо вентилятори й вмикаються, то ненадовго. |
| 7 | Д2 | Air movement, even in a closed greenhouse, helps reduce moisture on the plant surfaces and surrounding the plants. | Рух повітря навіть у закритій теплиці зменшує вологу на рослинах і навколо них. |
| 7 | Д4 | Circulating fans serve to reduce disease incidence by keeping any humidity from settling over the plant leaves. | Циркуляційні вентилятори зменшують захворюваність, не даючи волозі осідати на листі. |
| 8 | Д1 | Microcracking or Russetting: when the air temperature is increased quickly | Мікротріщини плодів виникають, коли температуру повітря підвищують швидко. |
| 9 | Д1 | High night temps increase respiration which wastes photosynthates reducing yield potential. | Висока нічна температура посилює дихання, витрачає продукти фотосинтезу й знижує врожайність. |
| 9 | Д1 | If RH is low, plants may transpire too much and wilt (i.e., mid-day wilt). | За низької вологості рослини надмірно випаровують воду й в’януть (полуденне в’янення). |
| 9 | Д2 | Always water in the morning to reduce the length of time the leaves stay wet after irrigating. | Завжди поливайте зранку, щоб листя після поливу менше часу залишалося мокрим. |
| 10 | Д3 | When daytime temperatures exceed 85 degrees F or nighttime temperatures exceed 70 degrees F, pollination suffers | Коли вдень температура вище 29 °C або вночі вище 21 °C, запилення погіршується. |
| 10 | Д1 | Flower Drop: may be due to temperatures over 33C (90F) or below 10C (~50F), | Опадання квіток може бути спричинене температурою вище 33 °C або нижче 10 °C. |
| 11 | Д4 | Tomato, “Flowering-harvest 70-75°F 85°F 65°F” (табл. 1: оптимум, максимум, поріг вентиляції) | Томат, цвітіння–збирання: оптимум 21–24 °C, максимум 29 °C, поріг вентиляції 18 °C (для фази розсада–цвітіння поріг 24 °C). |
| 11 | Д5 | adequate outside air must be introduced to insure complete combustion. | Для повного згоряння потрібно подавати достатньо зовнішнього повітря. |
| 12 | Д4 | disease problems can occur above 85 percent relative humidity (RH). | Проблеми з хворобами можуть виникати за вологості понад 85 %. |
| 12 | Д2 | relative humidity of 93% or greater | відносна вологість 93 % і вище (умова розвитку сірої гнилі) |
| 12 | Д2 | a film of moisture for 8 to 12 hours | плівка вологи протягом 8–12 годин |
| 12 | Д3 | The ideal relative humidity range for pollination of tomato is 40 to 70 percent. | Ідеальна вологість для запилення томата — 40–70 %. |

## 5. Інформаційні одиниці

Таблиця одиниць, суперечностей і прогалин: [knowledge/units.md](../knowledge/units.md).
