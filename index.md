# Фишки Inkscape
<!-- copyright: ReSampled 3 -->

# Effects
## Film grain

<iframe width="560" height="315" src="https://www.youtube.com/embed/f2c9shGMlTA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/CI670zWWB5o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/Aq9FEXSqxaU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Node tool
## Change segment(s)
(These commands require that more than two adjacent nodes be selected)

Shift+L - make line


Shift+U - make curve

## Change node type
Shift+C
make cusp
First Shift+C changes type of node; if you do another Shift+C on an already cusp node, it retracts its handles.

Shift+S
make smooth
If a cusp node is adjacent to a line segment, first Shift+S makes it half-smooth with one handle collinear with the segment; another Shift+S will expand a second handle.

Shift+Y
make symmetric
When making smooth or symmetric, you can lock the position of one of the handles by hovering mouse over it.

Shift+A
make auto

Ctrl+Left Mouse click
toggle smooth/cusp/symmetric/auto

-----

# Inverting colours

Note that Filters->Color->Invert... will work regardless of whether it's a raster or not. If it's a vector image made up of several parts it will be easier to group them all first.

But there's a big caveat: filters are a raster effect applied at the point of rendering your image. They do not alter the underlying geometry or data of the vector objects. If your requirement is just to export an inverted PNG this should work fine. If, however, the SVG file has to go to another program that expects black and white fills on the vector objects, filters won't do the job. In that case Extensions > Colour > Negative should do the job.

---------

# Object
* F1 → Перейти в режим вращения → зажать *Ctrl* → потянуть уголок → **поворот на 15 градусов**
* F1 → Перейти в режим вращения → зажать *Ctrl* → потянуть между уголками - **skew (изометрия) - с привязкой**
* F1 → Перейти в режим вращения → зажать *Shift* → потянуть уголок → **поворот относительно противоположного уголка без привязки**
* F1 → Перейти в режим вращения → зажать *Shift* → потянуть между уголками → **skew (изометрия) - без привязки**
* F1 → Перейти в режим вращения → зажать *Ctrl/Shift* → потянуть уголок - **поворот относительно противоположного уголка c привякой**
* F1 -> Перейти в режим вращения → зажать *Ctrl/Shift* → потянуть между уголками → **skew (изометрия) - с привязкой, только та сторона, которую перемещают**
* F1 → режим масштабирования → зажать *Ctrl* → **масштабирование с сохранением соотношения сторон**
* F1 → режим масштабирования → зажать *Shift* → **масштабирование без сохранения соотношения сторон, отличается от масштабирования без *Shift***
* Центр вращения объекта можно изменить, для этого нажмите на объект, чтобы появились стрелки вращения. В центре объекта будет находится крестик - это и есть центр вращения. Его можно перенести в любую точку.
* Для более точного задания трансформаций можно воспользоваться панелью **Трансформировать** *(Ctrl+Shift+M)*.
## Заполнить на основе клонов ([источник](http://sdemch.ru/Inkscape/_uroki_v_internet/ur_7_stakan_soka/copy_zdn_7_from_internet/stakan_s_sokom.htm))
Воспользуемся возможностью inkscape **"Создать узор из клонов"**, которая находится в меню **"Правка" → "Клоны"**. Inkscape запоминает последние настройки, поэтому, на всякий случай, нажмите кнопку **"Сбросить"**, что бы отменить старые настройки. Когда настройки установлены по умолчанию на закладке **"Обводка"** отметить **Размер**, **Наличие** и строк и столбцов по 10:

![image](http://p.resampled.ru/popd-b62fc87eb470c528d17889a96ec8c489.png)

А на вкладке **"Масштаб"** параметры случайности 100%:

![image](http://p.resampled.ru/popd-90d2e1d3685ab045e10585a54b009de6.png)

Теперь нажмите кнопку **"Создать"** и если результат примерно соответствует вашим ожиданиям, то придайте некий хаос, нажимая кнопку **"Разровнять"**. Если получилось совсем не то, что вы ожидали, поэкспериментировав с размером исходного объекта или настройками узора. Для того что бы отменить неправильный узор, нажмите кнопку **"Удалить"**.

## Сделать штриховку ([источник](http://pedcollege.com/?page_id=4031))
Нарисовать одну линию. Сделать несколько ее дублей *(Ctrl+D)*, а потом расставить их равномерно с помощью диалога в главном меню **«Объект» → «Выровнять и расставить»** *(Shift+Ctrl+A)*. Сгруппируйте получившиеся линии в группу *(Ctrl+G)* и разместите на объекте, который хотите заштриховать.


![image](http://p.resampled.ru/popd-691a8b1e30162113a96874eef0b8c396.png)

Можно сделать дубль узора и разместить еще где-нибудь на штрихуемом объекте. После того как линии будут размещены, сделайте дубль штрихуемого объекта *(Ctrl+D)*. Выделите линии и дубль штрихуемого объекта и в главном меню **"Объект" → "Обтравочный контур" → "Установить"**.

![image](http://p.resampled.ru/popd-4589d6a3ea6603741700d106193d9ffd.png)

## Карандашный набросок ([источник](https://inkscape.paint-net.ru/?id=38))
Когда контур выделен, примените к нему контурный эффект "карандашный набросок" (**"Контур" → "Редактор контурных эффектов"** или *Shift+Ctrl+7*) .

![image](http://p.resampled.ru/popd-98eb1dfb9159df90c425d7a0e571ef52.png)

<iframe width="560" height="315" src="https://www.youtube.com/embed/7rEnrc0wh5I" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

-----------


## Внутренняя штриховка ([источник](https://inkscape.paint-net.ru/?id=38))
Создайте контур и сделайте его копию *(Ctrl+D)*. Далее — **"Контур" → "Редактор контурных эффектов"** или *Shift+Ctrl+7*. Выберите эффект "Внутренняя штриховка" (“Hatches (rough)“) и нажмите кнопку **"Добавить"**.

![image](http://p.resampled.ru/popd-c1703560a17d0697e943ed737334267a.png)

Если теперь выделить штриховку инструментом управления узлами *(F2)*, то вы увидите несколько управляющих маркеров. С помощью этих маркеров и параметров эффекта можно управлять свойствами штриховки.

![image](http://p.resampled.ru/popd-aa1330dc5265bee1c1876d406eb95e33.png)

## Переключение между перекрывающимися объектами
С точки зрения работы огромные трудности вызывают перекрывающиеся объекты. Переключаться между ними можно, удерживая клавишу *Alt*.

## Отражение
Выберите контур. Далее — **"Контур" → "Редактор контурных эффектов"** или *Shift+Ctrl+7*. Выберите эффект "Зеркальная симметрия" (“Hatches (rough)“) и нажмите кнопку **"Добавить"**.

![i](http://p.resampled.ru/popd-01fb183e1cfe19b46def1e0749431c89.png)

Выберите **Free from reflection line** и нажмите *F2* чтобы управлять смещением отражения. Выберите **Fuse paths**, чтобы “склеить” обе части.

![image](http://p.resampled.ru/popd-0103fc5335d386bdc9d9ae5a32830267.png)

-----
# Прочее
## Направляющие
Тянем за линейку и достаем. Если нажать *Shift* и навести - можно поворачивать (с *Ctrl* — с привязкой). Двойной клик открывает точную настройку направляющей.
Что бы сделать наклонную направляющую, можно сразу сделать наклонную направляющую из угла линейки. Эта направляющая будет под углом 45 градусов.

![image](http://p.resampled.ru/popd-beed113b334527be98f2875cc3265775.png)

# Горячие клавиши
https://inkscape.org/doc/keys.html

-----
# Источники
* <http://www.inkscape.sdemch.ru/indexinkscape.htm>
