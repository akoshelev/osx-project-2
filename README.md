Проект 2. Тайм-трекер для MacOS совместимый с LazyCure
=============

Задача
------------------------
При работе с несколькими заказчиками, которые предпочитают оплату time-material часто требуется знать сколько конкретно часов было посвящено той или иной активности (задаче). Как правило считать эти часы вручную неудобно, поэтому и существует класс программ, которые эту задачу решают. 
Автор в своей работе использует тайм-трекер [LazyCure](http://lazycure.com/) клиент которого существует только под Windows. Задача сводится к разработке неполного аналога под MacOS.

Принцип работы и организации взаимодействия с пользователем
------------------------

Типичный вариант использования приложения выглядит следующим образом:

1. Запуск приложения вызывает старт таймера и начинается отсчет времени.
2. Пользователь, закончив какую-либо задачу, вводит ее название в поле "Task" и нажимает кнопку "Done".
3. Программа сохраняет информацию о названии, времени начала и продолжительности задачи в XML файл.
4. Приложение перезапускает таймер и отсчет времени начинается сначала.

Особенности:

1. Приложение должно располагаться в меню-баре.
2. Приложение должно хранить список введенных названий задач и предлагать их к выбору при вводе начальных букв (autocomplete).
3. При попытке закрыть приложение, не сохранив данные о последней активности, приложение должно выдавать диалоговое окно с предложением их сохранить.
4. XML файлы должны создаваться для каждого дня отдельно, при переходе через полночь, задача должна разбиваться на две части и записываться в два разных файла.
5. Формат XML файлов должен быть полностью совместим с форматом файлов LazyCure.
6. Приложение не должно предлагать средств просмотра данных файлов.

Аудитория
------------------------
Пользователями данного приложения является широкий круг лиц, работа которых предполагает накапливание и анализ данных о задачах, которыми им приходится заниматься, в том числе:

- разработчики программного обеспечения;
- инженеры по качеству (QA);
- проектные менеджеры.
