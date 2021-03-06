# Всегда используйте объектно-ориентированное программирование. #

> Проблема объектно-ориентированных языков в том, что они тянут за собой всё, что с ними связано. Вы хотели банан, а получили обезьяну, его держащую, и еще все джунгли в придачу.
>
> -- Джо Армстронг в [«Кодеры за работой - Размышления о ремесле программирования»](http://codersatwork.com/)

> Абстракция – великая сила. А что у меня вызывает аллергию еще с 1990-х, так это CORBA, COM, DCOM и всякая объектно-ориентированная чушь. Каждый новый проект в то время обязательно имел какую-нибудь примочку, которой было нужно 200 000 вызовов только для того, чтобы напечатать Hello World. Это профанация. Настоящие программисты таким не занимаются.
>
> -- Брендан Айк в [«Кодеры за работой - Размышления о ремесле программирования»](http://codersatwork.com/)

Многие разработчики программного обеспечения и многие компании считают, что объектно-ориентированное программирование сегодня является единственным разумным способом разработки. Любой, кто выступит против него, сразу же осознает тот факт, что он спорит против «традиционной мудрости».

На блогах и форумах по программированию есть очень много людей, которые отстаивают ООП, и которые уверены, что знают, о чем говорят. И это несмотря на отсутствие какого-либо четкого его определения!

Дело в том, что так называемое объектное программирование зачастую становится тяжелым бременем из-за ненужной сложности!

Как компьютерные теоретики и программисты мы должны научиться опровергать предубеждения и находить лучшие решения для поставленной задачи.

На сегодняшний день одним из основных преимуществ PHP является поддержка обеих императивных, функциональной, объектно-ориентированной, процедурной и рефлексивной парадигм. PHP представляет собой огромный набор инструментов с большим количеством различных механизмов, которые позволяют решить многие проблемы по-разному, не только одним путем.

** Как только мы начинаем навязывать различные внутренние проблемы приложения одной специфической парадигме, мы перестаем думать творчески, перестаем работать эффективно.**

## Небольшой урок истории. ##

Один из лучших способов понять специфическую парадигму программирования – посмотреть на её эволюцию. Что послужило причиной для ее развития? Какие проблемы, имеющиеся в других парадигмах, привели к новому образу мышления? Была ли это реальная мировая проблема, либо она была академической? И как эта парадигма с тех пор изменилась?

Не имеет значения, что говорит человек X, и какое определение дает человек Y. Важна история возникновения парадигм.

> Есть два способа построения программ. Первый – сделать её настолько простой, что в ней очевидно не будет недостатков. Второй – сделать её такой сложной, что в ней не будет очевидных недостатков.
>
> -- [Чарльз Энтони Ричард Хоар](https://en.wikiquote.org/wiki/C._A._R._Hoare)

В прошлом, еще до пришествия объектно-ориентированных языков, примерно в конце пятидесятых, было создано множество программ с использованием неструктурированного программирования. Их иногда называют языками первого и второго поколений. Неструктурированное программирование исторически является самой ранней парадигмой. Её сильно критиковали за спагетти-код.

Существуют как высокоуровневые, так и низкоуровневые языки, которые используют неструктурированное программирование. К ним относятся ранние версии BASIC, COBOL, MUMPS, JOSS, FOCAL, TELCOMP, машинный код, ранние ассемблерные системы (без процедурных метаоператоров) и некоторые скриптовые языки.

Программа в неструктурированных языках, как правило, состоит из последовательных команд и операторов по одному в каждой строке. Строки обычно нумеруются либо имеют метки, позволяющие потоку переходить к любой строке в программе (например, с помощью непопулярного оператора GOTO).


В шестидесятые годы структурное программирование появилось в основном благодаря знаменитой  статье Эдсгера Дейкстры [«Доводы против оператора GOTO»](http://www.u.arizona.edu/~rubinson/copyright_violations/Go_To_Considered_Harmful.html)

Структурное программирование – это парадигма, которая улучшает ясность, качество и результат разработки программного обеспечения путем использования подпрограмм, блочных структур и циклов. В отличие от использования элементарных ответвлений программы, таких как оператор GOTO.

Позже из структурного программирования возникло процедурное. Оно основано на концепции «вызова процедур». А это просто другое название «вызова функций». Процедуры так же известны как подпрограммы или методы. Процедура просто содержит ряд вычислительных шагов, которые должны быть выполнены. Любая процедура может быть вызвана в любой момент во время выполнения программы, в том числе и другими процедурами или даже собой.

Вначале все процедуры были доступны из любой части программы в качестве глобальных данных. В небольших программах это не представляло проблемы, но, как только программа усложнялась, и ее размер увеличивался, небольшие изменения в одной части программы стали в значительной степени влиять на многие другие части.

Никто не планировал таких изменений и появления такого количества зависимостей. Небольшое изменение в одной процедуре могло привести к череде ошибок во многих других процедурах, зависящих от её исходного кода.

Новая технология развивалась, что позволило разделить данные на разные области видимости, называемые «объектами». Только конкретные процедуры, относящиеся к одной области видимости, могли получить доступ к данным той же области. Это называется скрытие данных или инкапсуляция. Результатом стала намного лучшая организация кода.

Сначала объекты не назывались объектами, они рассматривались только как области видимости. Позже, когда зависимости и связи между переменными и процедурами внутри этих областей уменьшились, их стали рассматривать как отдельные изолированные сегменты. В результате родились такие понятия, как объекты и объектно-ориентированное программирование.

Еще позднее, в основном благодаря развитию Java, появились некоторые «словечки», процедуры и функции перестали называться функциями, а стали называться методами, если они находились внутри границ объекта. Переменные тоже больше не называют «переменными», они были переименованы в «атрибуты», если они находились в отдельной области видимости.

Таким образом, объект, по сути, это просто набор функций и переменных, которые теперь стали называться «методами и атрибутами».

Методы и атрибуты изолированы внутри отдельной области с помощью использования «класса». После создания экземпляра класса он называется объектом.

Объекты могут друг на друга ссылаться, и с помощью этих ссылок методы (функции) внутри могут «общаться» друг с другом. Объекты могут также «перенимать» методы от других объектов, тем самым их расширяя. Это называется «наследованием». Это способ повторного использования кода, позволяющий создавать независимые расширения программ через публичные классы и интерфейсы. Взаимосвязи объектов приводят к иерархии. Наследование было изобретено в 1967 году для языка программирования [Simula 67](http://en.wikipedia.org/wiki/Simula).

Объекты могут так же наследовать методы от других объектов и «переопределить» их с добавлением или изменением функциональных возможностей. Это называется «полиморфизм».

Эти в разных языках программирования эти идеи реализованы разными способами.

Объектно-ориентированное программирование – это совершенно другой способ организации кода, чем был раньше. Это продолжение процедурного программирования с добавлением сокрытия данных (инкапсуляции) и избеганием глобальных областей видимости. Речь идет о расширении функций путем «заимствования» своих схем без влияния на исходный код (наследование). И речь идет о переопределении функций, при котором не затрагивается исходный код (полиморфизм).

> Объектно-ориентированная модель позволяет легко наращивать программы за счет аккреции. На практике это, как правило, означает, что она обеспечивает структурированный способ записи спагетти-кода.
>
> -- Пол Грэм в [Ansi Common Lisp](https://openlibrary.org/works/OL7944696W/ANSI_Common_Lisp)

**Неправильный путь**: Всегда использовать объектно-ориентированное программирование. ![Thumbs down](/img/thumbs-down.png)
