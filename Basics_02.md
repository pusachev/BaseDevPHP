# 2. Змінні, Булева алгебра, двійкова арифметика

## Змінні та типи даних.

Результат роботи програміста – програмний код, текст. Код складається з інструкцій комп'ютера, які, як і в якій послідовності виконати. Всі ці інструкції дотримуються певної мети, яку бачить програміст. Початкові, проміжні та кінцеві дані кожної дії або комплексу дій зберігають у змінних, які мають певний тип даних. Для того, щоб розуміти весь цей процес, ми наше знайомство з програмуванням почнемо з кількох термінів:

**Змінна** - дані, які зберігаються в оперативній пам'яті та мають ім'я та тип. Простіше асоціювати з підписаним контейнером, у якому щось лежить.

** Тип даних ** - характеристика набору даних, яка визначає можливі значення цього набору, ряд допустимих операцій, які можна робити з цими даними, та спосіб зберігання цих даних у пам'яті.

*Приклад із реального життя:*
>Коробки з фруктами, у яких написано " Фрукти " . Вони займають певне місце, має назву і всі приблизно орієнтуються, що можна зробити з вмістом цієї коробки. Коробки із фруктами містять фрукти. Їх можна відкрити, фрукт можна з'їсти, можна розрізати, можна почистити, можна приготувати салат тощо.
>Ящик з написом "Посуд" при переїзді. Ясно, що всередині тендітне і б'ється, ясно, як це транспортувати і коли розпаковувати.

У програмуванні типів даних багато, й у різних мовах вони різняться. Тим не менш, розглянемо їх загальні види та характеристики. Розібравшись із цим, ми зможемо класифікувати будь-який незнайомий нам тип даних.

![Не вчи типи, дизайнер!](http://memesmix.net/media/created/1z591q.jpg)


**Примітивами** називають типи даних, які складаються з одного елемента. Синоніми до цього визначення - "скалярні".

**Структурними** можна назвати типи даних, які з елементів інших типів даних. Назва – синонім: нескалярні, аггрегатні.

Простіше кажучи, примітиви - найпростіші типи даних, які є неподільними, тоді як структурні складаються з набору структурних або примітивних типів.

### Скалярні типи даних або примітиви.

Багато, якщо не в усіх мовах програмування високого рівня зустрічаються такі примітиви:

- **Булеві або логічні дані.** Змінна цього типу може мати тільки два значення - Правда і Брехня (**True, False**). Часто ці параметри інтерпретуються відповідно як 1 і 0. Використовується повсюдно щоб одержати відповіді різні питання та подальшого вибору варіанта дій.
- **Цілі числа.** Змінні такого типу містять ціле число. Залежно від мови програмування та обраного підтипу цілих даних розрізняються діапазоном значень та можливістю роботи з негативними числами.
- **Числа з плаваючою точкою** чи речові числа. Сюди входять як цілі числа, у яких дрібна частина є, але вважається порожньою, так і дрібні. У програмному вигляді найчастіше такі числа записуються як `x = a * 10^b`, тобто. через дробове десяткове число **a**, помножене на 10 ступенем **b**. У математиці це як "1.2*10^3", в програмуванні ступінь числа 10 пишеться через експоненту, тобто. `1.2e3`. Наприклад, відстань від Землі до Сонця становить `1.496 · 10^11`, або 1.496e11.
- **Комплексні числа** - числа виду `x + iy`, де `i` - корінь із мінус одиниці. Потрібно для низки математичних процесів і пошуків, простому програмісту знадобиться досить рідко.
- **Відсутність значення та типу** - особливий тип даних, який означає нічого, порожнє місце. Відрізняється від нуля, порожнього рядка чи порожнього масиву. У різних мовах називається по-різному, наприклад null, none, nan.
- **Рядки** - Рядки прийнято відносити до примітивів, хоча вони і складаються із символів.

### Структурні типи даних.

Структурні типи даних, які можна зустріти різними мовами:

- Масиви
- Кортежі
- Словники
- Mножини
- функціональні типи даних
- Записи

Ці типи даних ми розглянемо пізніше докладніше.

### Мутабельність (mutable)

Так само типи даних можуть бути змінними або **мутабельними**, і незмінними (**іммутабельними**). Знайомлячись з новими типами даних конкретної мови розумно було б з'ясовувати, чи можна його змінювати, чи він іммутабельний, тобто. значення його залишиться тим самим, яким було створено, і можна або працювати з тим значенням, що є, або створювати нове значення для нього.

Ті ж рядки, наприклад, можуть бути незмінними. Це означає, що в змінну можна записати рядок, але змінити його буде неможливо. Однак, буде можливість записати в цей змінний інший рядок, у тому числі змінений вихідний рядок.

### Булеви змінні

Змінна типу `bool` може містити лише два значення: **True** або **False**, причому це не рядки, не числа, а саме поняття брехня та істина.

Для роботи з змінними булевими існує булева алгебра.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/George_Boole.jpg/267px-George_Boole.jpg)

### Булева алгебра (логічні оператори)

Існують такі логічні оператори:

* and - І
* or - АБО
* xor - Виключає АБО (підключається окремо)
* not - НЕ

not означає НЕ, і, будучи поставленим перед типом bool, змінює його значення зворотне, тобто. **`not True`** стає **`False`**,**`not False`** стає **`True`**

Далі наведено таблицю, яка демонструє роботу операторів:

| Оператор  | 0 to 0| 0 to 1| 1 to 0 | 1 to 1|
|-----------|:-----:|:-----:|:------:|:-----:|
| and або `&&` |   0   |   0   |    0   |   1   |
| or        |   0   |   1   |    1   |   1   |
| xor       |   0   |   1   |    1   |   0   |


### Оператор умови "якщо" (if)

У багатьох, якщо не в усіх мовах програмування, існують умови виду **якщо - інакше, якщо - інакше**. Код виглядає приблизно так:

````
якщо (X mod 2 == 0):
     число непарне
інакше:
     число парне
````
Операція mod – операція взяття залишку від розподілу.

Є різні варіанти використання оператора `якщо`: просто `якщо`, з використанням `інакше` і з будь-якою кількістю `інакше, якщо` між `якщо` та `інакше, якщо`.

### Тернарні оператори

Багато мовами програмування (С++, Java, PHP...) існують тернарний оператор, тобто. спеціальний оператор умови, який повертає один із двох результатів, залежно від того, виконується його умова чи ні. Виглядає він так:

````
повідомити (Час доби = 'ранок') ? "Вітання!" : "Бувай!";
````

Тернарні оператори часто застосовуються, коли варіанти всього два, тому що такий запис коротший за аналогічну дію з `якщо`. Однак, на жаль, можна зустріти зв'язку кількох "якщо" та тернарних операторів, яку абсолютно неможливо прочитати. Іншими словами, це не потрібна річ у мові і вона може стати причиною нечитаного тексту.

### Множини

Множина або сет (set) по суті - "контейнер", що містить унікальні елементи, що не повторюються, у випадковому порядку. У цьому вся визначенні згадані дві основні особливості сетів - **унікальність** і **відсутність сортування**.

Унікальність - сет містить лише унікальні елементи, якщо додавати до нього дублікати - вони не додаються, якщо перевести якусь змінну з неунікальними даними в сет - дублюючі елементи будуть видалені.

Відсутність сортування - елементи в сеті знаходяться в певному хаотичному порядку.

Множини підтримують перебір всіх елементів (ітерацію), додавання та видалення елементів, але в силу відсутності сортування не підтримують індексацію та зрізи.

Створення множин:

````
м1 = множина([1, 2, 3, 4, 5, 6])
м2 = множина([5, 6, 7, 8, 9])

a = [1, 2, 3, 4, 5, 6, 5, 4, 3, 2]

вивести a
[1, 2, 3, 4, 5, 6, 5, 4, 3, 2]

м3 = множина (a)

вивести м3
([1, 2, 3, 4, 5, 6])
````

Множинa підтримує операції віднімання, об'єднання, перетину:

````
м1 = множина([1, 2, 3, 4, 5, 6])
м2 = множина([5, 6, 7, 8, 9])
м1 - м2 # Різниця множин
([1, 2, 3, 4])

м1 | м2 # Об'єднання множин
([1, 2, 3, 4, 5, 6, 7, 8, 9])

м1 & м2 # Перетин множин
([5, 6])
````

Можна додати елемент до множини і видалити з множини елемент. Як параметр виступає сам елемент, оскільки індексів у множині немає.

````
м1.додати(7)

вивести м1
([1, 2, 3, 4, 5, 6, 7])

м1.видалити(1)

вивести м1
([2, 3, 4, 5, 6, 7, 8])
````


### Діаграми Ейлера-Венна

![](images/krugi.jpg)

Множини прийнято візуалізувати за допомогою діаграм Ейлера-Венна.
У тому числі і алгебру булеву зручно і просто зрозуміти на прикладі таких діаграм:

**AND, і в тому і в тому випадку істина:**
![](images/and.png)

**OR, або в тому чи в тому випадку істина:**
![](images/or.png)

**XOR, істина або в тому, або в іншому випадку, але не в обох випадках відразу.**
![](images/xor.png)


### Практичні завдання на діаграми Ейлера-Венна

**1. Намалювати кола для заварної кави:**

- еспресо
- американо
- капучіно
- Латте
- доппіо

**3. Вирішити завдання:**
Усі жінки – доньки, але не всі жінки матері. Деякі матері – бабусі. Намалюйте онучок!

**5. Розмістити у колах:**
Всього Студентів 2000

Програмістів 1500

Дизайнерів 300

Менеджерів 200

Фронтендників 1000

Бекендників 500

PHP програмістів 200

JS програмістів 1200

Java програмістів 100

## Системи числення

І насамкінець трохи поговоримо про системи числення, це нам неодноразово знадобиться у розумінні деяких концепцій програмування у майбутньому.

![Системи числення](http://sc109.ru/content/distant/inform/6/6klass_kod_info/images/ss.png)

Для кращого розуміння програмування буде не зайвим вміти читати числа різних систем числення та перекладати з однієї в іншу.

![](http://atkritka.com/upload/iblock/de4/atkritka_1521038238_454.jpg)

## Корисні посилання

Дод. статті:

[Кола Ейлера](https://blog.tutoronline.ru/krugi-jejlera)

[Математична логіка](http://ya-znau.ru/znaniya/zn/135)

[Рішення задач за допомогою кіл Ейлера](https://sibac.info/shcoolconf/science/xvii/42485)

[Тест на логічне мислення](http://testoteka.narod.ru/pozn/1/10-on.html)

[Онлайн створення діаграм](https://creately.com/ua/%D0%9A%D0%BE%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1 %82%D0%BE%D1%80-%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC-%D0%92%D0 %B5%D0%BD%D0%BD%D0%B0-%D0%BE%D0%BD%D0%BB%D0%B0%D0%B9%D0%BD)

[Двійкова система числення - найпростіше пояснення](https://www.youtube.com/watch?v=RcxvcLl1nAs&ab_channel=ZerotoHero)

[Шістнадцяткова система числення](https://www.youtube.com/watch?v=AkXHkwVCcRU&ab_channel=ZerotoHero)

## Домашка

[Домашнє завдання](hw2.md)