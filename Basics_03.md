# 3. Перераховані типи даних, цикли, основи функцій.


## Змінювані та незмінні типи даних

Як ми вже обговорювали, існують типи даних, що змінюються (**mutable**) і незмінні (**immutable**).

Раніше розглядався цілий тип даних, який, часто, є незмінним. Також незмінними можуть бути типи даних **tuple** (кортеж) і **string** (рядок).

Що означає незмінними? Отже, спочатку створений рядок ми змінити не можемо. Якщо ж здається, що об'єкт однієї з перелічених даних змінився - отже тепер ім'я об'єкта просто вказує нову область у пам'яті з новим об'єктом.

## Рядки

У деяких мовах є різниця між одинарними та подвійними лапками, у деяких є, а трапляються ще й потрійні лапки двох видів, і все це – для створення рядків. Проте тут немає нічого складного, основне правило при створенні рядка: яким видом лапок ви почали створювати рядок, таким і закінчуйте.

````
s = 'asdf'
````
Ось типове створення рядка.

![](https://study.com/cimages/multimages/16/java_string_object.png)

Найпростіші арифметичні операції додавання та множення часто доступні і з рядками. Додавання двох рядків називається **конкатенацією**.

![](images/concat.jpg)

  У деяких мовах існує множення рядка на число та взяття конкретного елемента рядка за його індексом. Індекси у всіх послідовностях у програмуванні вважаються від нуля. Деякі ЯП дозволяють працювати за негативним індексом – відраховуємо від кінця послідовності назад.


## Масиви, списки, кортежі

У різних ЯП існують різні типи послідовностей. Ті типи, в яких кожен елемент має порядковий номер, називаються **масивами**.

Масив може бути **гомогенным**, тобто. містять дані лише одного типу, і **гетерогенним**, тобто. містить різнотипові дані.

Трапляються мови, що містять обидва типи, зустрічаються і ті, в яких можливий лише один тип масиву.

Залежно від розмірності масиву розрізняють **одномірні та багатовимірні** масиви.

![](http://images.myshared.ru/4/222475/slide_4.jpg)

![](http://study-java.ru/wp-content/uploads/2014/03/array.png)

Також масиви може бути змінюваними, тобто. **мутабельними**, і незмінними, тобто. **іммутабельними**.

### Операції з масивами

Створюються масиви за допомогою:

- перерахування елементів відразу під час створення
- додавання елементів у циклі після обробки якогось джерела чи обчислень
- з інших типів даних, наприклад, з рядків
- спеціальними генеруючими функціями.

Крім створення масивів, класичними операціями з масивами є:

- додавання елементів на початок, кінець або будь-яке місце масиву (якщо він мутабелен)
- взяття елемента за індексом
- взяття підмасиву
- видалення елемента або підмасиву
- Сортування різних видів

Найчастіше з масивами працюють з допомогою різних циклів, або за кількістю елементів у масиві, або перебираючи їх поэлментно.

### Словники

Є окремий вид масивів, який називають асоціативним масивом чи словником. Хеш – ще один синонім для такого типу даних. Це теж складовий, структурний іп даних, але ключем тут можуть виступати не лише числа, а й рядки, а в деяких мовах – і дугі типи даних. Значенням, зазвичай, можуть бути всі існуючі типи даних.

![](https://o7planning.org/en/11437/cache/images/i/7722025.png)

Існує кілька варіантів створення словників, і вони пожертвують більшість операцій, які прийдуть на думку програмісту:

- Розширення одним елементом
- Розширення словником
- Видалення елемента по ключу
- взяття всіх ключів
- взяття всіх значень
- ... та багато інших дій.

### Цикли

Найважливішим елементом багатьох ЯП є цикли.

Для їх розуміння важливі такі терміни:

**Тіло циклу** - дії, що виконуються в рамках циклу. Зазвичай укладені у фігурні дужки або їх аналоги і розташовані нижче та зі зсувом, у разі циклу з постумовою - вище та зі зсувом.
**Ітерація** - один прохід тіла циклу.

Поширені такі варіанти циклів:

1. Цикл із передумовою. Найчастіше це **while**. Як правило, такий цикл перевіряє умову, і якщо вона істинна, виконує ряд дій, що знаходяться в тілі циклу. Потім знову перевіряє умову, виконує ті ж дії, і так доти, доки умова не стане хибною.

2. Цикл з постумовою – зустрічається та використовується дещо рідше. Найчастіше називається **do while** Дуже схожий на перший варіант, але завжди виконує одну ітерацію циклу до перевірки умови. Простіше кажучи, спочатку робить всі дії один раз, потім перевіряє умову і виконує ці дії знову і знову, поки умова істинна. Якщо ця умова спочатку помилкова, цикл із постумовою спрацює один раз, тоді як цикл із передумовою - жодного разу.

3. Цикл із лічильником. Найчастіше це **for**. Ісользується для того, щоб повторити деякий набір дій – тіло циклу – певну кількість разів. Як правило, у самому заголовку циклу визначається змінна, умови її зміни та умова перевірки, чи не досягла ця змінна граничного значення, коли цил повинен припинити виконуватися.

4. Цикл перебору. Варіанти назв: **for, foreach, each**. Служить для того, щоб поелементно працювати з масивами або іншими типами даних, що перераховуються.

### Функції

Функціями називаються окремі блоки коду. Найчастіше ці блоки мають імена, вони виконують певні дії і повертають результат. Причини, через які програміст може виділити частину коду в окрему функцію, зазвичай такі:

- цей код з'являється та виконується у різних місцях програми
- Цей код має чітке призначення
- Цей код має досить складну логіку

Вже буквально на наступному уроці ми познайомимося з PHP, через урок-другий познайомимося з функціями і почнемо розуміти існуючі функції, так і писати свої власні.


## Домашка

[Домашнє завдання](hw3.md)
