## Федеральное агентство по образованию РФ

## Дальневосточный федеральный университет

## Институт математики и компьютерных технологий
## Департамент информационных и компьютерных систем
## Отчёт о практическом задании по предмету Программная инженерия

# Хоррор-игра на Unity

### Федотов И. Н.
### Мельников С. В.
### Курышев В. И.
Б9121-09.03.03пикд

## Владивосток, 2023 г. 

Введение
========

Глоссарий
---------
Бандл — комплект, состоящий из нескольких товаров, продаваемых как единое целое.

Геймплей — компонент игры, отвечающий за взаимодействие игры и игрока. Геймплей описывает, как игрок взаимодействует с игровым миром, как игровой мир реагирует на действия игрока и как определяется набор действий, который предлагает игроку игра.

Игровой движок — базовое программное обеспечение компьютерной игры. Разделение игры и игрового движка часто расплывчато, и не всегда студии проводят чёткую границу между ними. Но в общем случае термин «игровой движок» применяется для того программного обеспечения, которое пригодно для повторного использования и расширения, и тем самым может быть рассмотрено как основание для разработки множества различных игр без существенных изменений. 

Скример — внезапно появляющийся страшный кадр в фильмах ужасов, видеороликах, компьютерных играх и т. п., сопровождаемый пронзительным криком или другим пугающим звуком.

Текстура — обычное изображение, которое накладывается на поверхность готовой модели, чтобы придать ей цвет, свойства и рельефность.

Туториал — пошаговая инструкция по выполнению какого-либо процесса, учебное пособие, познавательный обучающий материал

Шейдер — небольшая программа, содержащая инструкции для GPU. Она описывает способ вычисления экранного цвета для определенного материала. 

GUI — интерфейс, элементы с которыми взаимодействует пользователь: кнопочки, плашечки, бары; элементы навигации, подсказки, и т.п.

Unity — кроссплатформенный игровой движок, разработанная американской компанией Unity Technologies.

Unreal Engine — игровой движок, который был создан в 1998 году, компаний Epic Games.

Описание предметной области
---------------------------
Область компьютерных игр появилась достаточно давно, развивается по сей день и пользуется широкой популярностью.  Компьютерные игры созданы для развлечения, и широко используются в коммерческих целях, а в некоторых странах игры признаны как предмет искусства, что позволяет им конкурировать с кино. Компьютерные игры могут быть различными: многопользовательские игры, промо-игры, программы, созданные с целью привлечь потенциального покупателя. Компьютерные игры могут быть созданы большими компаниями с большими финансами (AAA-проекты) либо небольшим коллективом без финансовой поддержки (инди-проекты) и имеют несколько жанров. В рамках данной работы будет рассмотрено создание инди-проекта в жанре “хоррор”.

Инди-игры, или игры, созданные небольшими командами или отдельными разработчиками, имеют довольно долгую историю. Их начало можно отследить еще в 1980-х годах, когда многие игры были созданы людьми, работающими из дома и распространялись через дисководы компьютеров. Однако, настоящий бум инди-игр начался только в 2000-х годах. С развитием Интернета и распространением цифровых дистрибьюторов игр, таких как Steam, эти игры стали легко доступными для потребителей. В 2005 году был основан сайт Kongregate, который стал одним из первых платформ для распространения браузерных игр, созданных независимыми разработчиками. Одной из первых популярных игр на этой платформе была "Desktop Tower Defense", созданная в 2007 году. В 2008 году была выпущена игра "World of Goo", которая считается одной из первых инди-игр, которая добилась большого коммерческого успеха. Она была создана небольшой командой разработчиков из США и продана в количестве более 2 миллионов копий. В последующие годы индустрия инди-игр продолжала расти и развиваться. В 2010 году была выпущена игра "Minecraft", которая стала одной из самых успешных и популярных игр всех времен. Она была создана независимым разработчиком из Швеции и продана в количестве более 200 миллионов копий. В 2012 году была выпущена игра "Journey", которая получила множество наград и стала первой игрой, которая была признана "Лучшей игрой года" на церемонии BAFTA. В последующие годы индустрия инди-игр продолжала расти и демонстрировать огромный потенциал. Некоторые известные инди-игры, выпущенные в последние годы, включают в себя "Undertale", "Stardew Valley", "Celeste" и "Hollow Knight". 

Сегодня индустрия инди-игр является одной из самых динамичных и успешных в мире видеоигр. Благодаря технологическому прогрессу и увеличению количества цифровых платформ для распространения игр, инди-игры стали еще более доступными для разработчиков и игроков. В настоящее время многие из них создаются в различных жанрах и на разных платформах, включая мобильные устройства, консоли и ПК. Одним из факторов, способствующих росту индустрии инди-игр, является их относительно низкая стоимость разработки и производства. Благодаря этому, разработчики могут сосредоточиться на творческом процессе и создании уникального геймплея и идей, не привязываясь к бюджетам больших студий. Однако, как и в любой индустрии, в инди-секторе есть свои проблемы. Одной из них является конкуренция и перенасыщение рынка, которые могут затруднить продвижение новых игр. Также некоторые игроки могут быть скептически настроены к играм, созданным независимыми разработчиками, считая их менее качественными, чем игры от больших студий. В целом, индустрия инди-игр продолжает расти и развиваться, привлекая все больше и больше разработчиков и игроков. Она становится все более разнообразной и интересной, предлагая новые и оригинальные игровые концепции и идеи, которые могут найти свою аудиторию среди игроков по всему миру.

Одним из таких примеров послужил феномен инди-хорроров в стилистике игр для Playstation One в начале 2020 года. На одном из самых популярных онлайн-сервисов для размещения игр itch.io появился бандл игр под названием "Haunted PS1 Demo Disc", в который входило 15 хоррор игр. Этот бандл не только сильно понравился игрокам, но и вдохновил разработчиков так, что даже в конце 2021 половина загружаемых хорроров на itch.io это игры с графикой игр для Playstation One.

Неформальная постановка задачи
----------------------------------------
В рамках данной работы необходимо разработать компьютерную игру в жанре инди-хоррор в графическом стиле игр для Playstation One. Для этого требуется: разработать сценарий, найти проектное решение, в данном случае движок, и готовые ассеты или разработка своих, изучение движка.

Политика распространения открытая, исходный код игры  опубликован на GitHub, а сам билд игры на itch.io доступен бесплатно.

Критерии сравнения:
* Качество сюжета
* Атмосфера и стиль
* Продолжительность
* Интересный геймплей
* Техническое исполнение

Инди-хорроры в стиле Playstation One.
1. Cry of The Mermaid — игра про заброшенный пассажирский корабль. Игра цепляет своей жуткой, меланхоличной атмосферой, интересными загадками и сюжетными записками. Время прохождения 30-45 минут.
2. The Touch — игра про молодую женщину с ребенком, которая осталась с ним одна глубокой ночью. Игра пытается продлить время прохождения путем низкой скоростью передвижения и напугать игрока скримерами. Время прохождения 3-5 минут.
3. MOTH HOUSE — игра, где нужно собирать большое количество мотыльков в очень темном заброшенном доме. Можно отметить очень интересную идею использования страха к насекомым, интересный визуальный стиль и техничность (реализован инвентарь, поимка мотыльков), но при этом отсутствует внятный сюжет, то есть игра сосредоточена на геймплее. Время прохождения 15-25 минут.
4. sleeping alone — игра, повествующая о 7-летнем мальчике, который заметил в доме призрака, в последствии убившего его родителей. Игра создает напряженную атмосферу, использует довольно простую, но цепляющую историю, знакомая каждому, кто боялся в детстве призраков, при этом не используя никаких скримеров. Время прохождения 10-15 минут.

|          Игра          | Качественный сюжет | Атмосфера и стиль | Продолжительность (минут) | Интересный геймплей | Техническое исполнение |
|:----------------------:|:------------------:|:-----------------:|:-------------------------:|:-------------------:|:----------------------:|
|   Cry of The Mermaid   |          +         |         +         |           30-45           |          +          |           +-           |
|       MOTH HOUSE       |         +-         |         +         |           15-25           |          +          |            +           |
|     sleeping alone     |         +-         |         -         |           10-15           |          -          |           +-           |
|        The Touch       |          -         |         -         |            3-5            |          -          |            -           |
| NIGHT OF THE CONSUMERS |          -         |         +         |           15-30           |          +          |            +           |
|      Peter's House     |          +         |         +         |           10-15           |          +          |            +           |
|        MemoRISE        |          +         |         +         |            5-10           |          +          |            +           |

Требования к окружению
======================
Для разработки компьютерной игры использован игровой движок Unity. В отличии от конкурента в виде Unreal Engine, движок Unity очень прост в освоении, что позволяет значительно сократить время разработки, а также не требует высоких системных требований как и для пользователя, так и для разработчика.

Понадобятся примерно следующие характеристики:
* ОС: Windows 7/8/10/11, MacOS, Linux
* Процессор: Любой 64-битный процессор
* Оперативная память: 4 ГБ ОЗУ
* Видеокарта: с поддержкой DirectX или OpenGL
* Место на диске: 100~ мб

Спецификация данных
===================
Формат файлов сохранений
------------------------
Формат файлов сохранений представлен в виде сериализованного JSON — формат файлов, который используется для хранения и передачи данных в легковесном, читаемом и легко редактируемом виде. Они обычно менее затратны по памяти, чем XML-файлы.

Функциональные требования
=========================
Система должна позволять пользователю:

в главном экране
* Начать игру
* Открыть настройки
* Выйти из игры

в экране паузы
* Продолжить игру
* Открыть настройки
* Выйти из игры

в настройках
* Поменять разрешение экрана
* Поменять настройки графики (низкие/средние/высокие)
* Поменять уровень звука
* Поменять уровень музыки
* Поменять чувствительность камеры

Требования к интерфейсу
=======================
Интерфейс должен:
* Интуитивно понятен игроку.
* Оптимизирован для большинства разрешений экрана с соотношением 16:10, 16:9 и 4:3.
* Интегрирован в игру как можно более органично, чтобы не отвлекать игрока от игрового процесса.
* Позволять игроку взаимодействовать с игровым миром.
* Позволять игроку настраивать графику, звук и другие параметры игры, чтобы создать максимально комфортные условия для игры.
* Обучать управлению персонажем.

Источники
=========
1. https://docs.unity3d.com/Manual/index.html

2. https://dtf.ru/indie/937127-fenomen-indi-horrorov-v-stile-ps1

3. https://shazoo.ru/2019/08/30/83887/psihologiya-straha-pochemu-vy-lyubite-igrat-i-smotret-horrory

4. https://ru.wikipedia.org/wiki/%D0%98%D0%B3%D1%80%D0%BE%D0%B2%D0%BE%D0%B9_%D0%B4%D0%B2%D0%B8%D0%B6%D0%BE%D0%BA

5. https://ks98.itch.io/cry-of-the-mermaid

6. https://kenforest.itch.io/moth-house

7. https://simvlz.itch.io/sleeping-alone

8. https://krieghor.itch.io/the-touch

9. https://germfood.itch.io/nightoftheconsumers

10. https://gzke.itch.io/peters-house
