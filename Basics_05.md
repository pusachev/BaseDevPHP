# 5. Стурктурні типи даних

**Массивы (array)** - структурований тип даних, що є просто впорядкованою послідовністю інших типів даних. У php, на відміну від багатьох інших мов, є всього один вид масивів, що поєднує в собі властивості різних структурних типів даних інших мов.

## Створення масивів

Масив чисел без зазначення індексів чи ключів:

```php
$ my_array = [1, 2, 3, 4, 5];
print_r($my_array);

/*Array
(
     [0] => 1
     [1] => 2
     [2] => 3
     [3] => 4
     [4] => 5
)
*/

// Починаючи з PHP 5.4
$array = [1, 2];
````
Масив рядків без зазначення індексів чи ключів:

```php
$cars = ['BMW', 'Opel', 'Audi'];
print_r($cars);

/*Array
(
     [0] => BMW
     [1] => Opel
     [2] => Audi
)*/
````
Масив чисел із використанням рядкового індексу:

```php
$marks = [
'Pupkin' => 5,
'Markov' => 2,
'Kichev' => 4,
];
print_r($marks);

*/Array
(
     [Pupkin] => 5
     [Markov] => 2
     [Kichev] => 4
)
/*

````

## Операції з масивом

Отримання елемента масиву, додавання елемента масиву:

```php
//додавання елемента в масив
$ arr = [1, 2, 3];
$arr[] = 4;
print_r($arr);
/*Array
(
     [0] => 1
     [1] => 2
     [2] => 3
     [3] => 4
)
*/

//Отримання елемента масиву
echo $arr[2]; // виведе 3
````
Двовимірний масив та отримання вкладеного елемента:

```php
$arr = ['z', 'x', ['aa', 'bb']];
print_r($arr);
echo PHP_EOL . $arr[2][0] . PHP_EOL;

/*Array
(
     [0] => z
     [1] => x
     [2] => Array
         (
             [0] => aa
             [1] => bb
         )
)
aa
*/

````
Видалення елемента масиву:

```php
$arr = ['x', 'y', 'z', ['aa', 'bb'], '11'];
print_r($arr);
/*Array
(
     [0] => x
     [1] => y
     [2] => z
     [3] => Array
         (
             [0] => aa
             [1] => bb
         )
     [4] => 11
)*/
unset($arr[3]);
print_r($arr);
/*Array
(
     [0] => x
     [1] => y
     [2] => z
     [4] => 11
)*/
````

Видалення масиву здійснюється функцією `unset`, застосованою до змінної масиву.


## Функції для роботи з масивами

* `unset` - видаляє масив або елемент масиву
* `array_values` - повертає всі значення масиву у вигляді масиву
* `array_keys` - повертає всі ключі масиву у вигляді масиву
* `array_map` - застосовує функцію, ім'я якої йде першим параметром у лапках, до всіх елементів масиву

Існує безліч функцій по роботі з масивами, ознайомитися з ними можна [тут] (http://php.net/manual/ru/ref.array.php) або в Google.


## Рядки

Рядок у php є найпростішим масивом символів. Наприклад, якщо змінну `$S` записано рядок `"Welcome"`, то `$S[3]` буде вказувати на символ c.

Рядки можна визначати як одинарними, так і подвійними лапками. Рядки в одинарних лапках вважаються трохи швидшими у роботі. Рядки ж у подвійних лапках дозволяють виводити деякі [escape-послідовності](http://php.net/manual/ua/regexp.reference.escape.php) та значення змінних, що вже згадувалося у першому уроці.


## Оператори циклу
Існують такі оператори циклу:

* while
* do while
* for
* foreach

У більшості випадків оператори циклу взаємозамінні, але кожен з них має деякі нюанси.

## Оператор while

Найпростіший оператор циклу while виглядає так:
`while (умова) дія`
або
`while (умова) {блок дій у кілька рядків}`

У минулих уроках ми вже мали приклади циклів while.

Суть роботи циклу: Перевіряється умова у циклі, якщо вона вповнюється (тобто `true`), тіло циклу виконується. Потім знову перевіряється умова циклу, якщо true - виконується тіло, і доти, доки перестане виконуватися умова циклу.

```php
$i = 10;
while ($i > 0) {
     echo $i-- . PHP_EOL;
}
````

## Оператор do while

Фактично той же цикл while, за одним уточненням: цикл завжди виконується хоча б один раз перед перевіркою умови.

`do (тіло циклу) while (умова)`

Той самий код але з циклом `do while`:

```php
$i = 10;
do {
     echo $i-- . PHP_EOL;
} while ($i > 0);
````

## Вічний цикл

У програмуванні часто використовуються вічні цикли. Просто є ситуації, коли немає явного обмеження і умову важко перевірити заздалегідь. Для того щоб вийти з вічного циклу, і взагалі з циклу, використовується оператор `break`. Він працює всередині циклу та припиняє його виконання. Далі проілюстровано роботу break і ще кілька операторів:

```php
$i = 10;
while (true) {
     if ($i % 2! = 0)
         echo $i. PHP_EOL;
     $i--;
     if ($i % 20 > -19) continue;
     if ($i <-10) break;
}
````

## Цикл for

Цикл `for` є поєднанням трьох дій і циклу. У дужках до першої точки з комою вказується початкова умова або умови, між першою та другою точкою з комою вказується умова, яку треба перевіряти перед кожною ітерацією циклу, а після другої точки з комою - дії, яку потрібно зробити кожен цикл:

```php
$limit = 10;
for ($i=1; $i < $limit + 1; $i++) {
         echo $i. PHP_EOL;
}
````

Цикл **for** багато в чому ідентичний циклу **while**, якщо подивитися на нього під певним кутом зору. По-суті, він так само, як і **while**, перевіряє певну умову, і за його дотримання запускає чергову ітерацію. Що додається, то це ініціалізація змінних до першої ітерації (початкові умови) та обов'язкові кожну ітерацію дії. Таким чином, **while** може замінити **for**, а **for** може замінити **while**. Це ми вивчимо практично.


## Цикл foreach

Цикл `foreach` є найбільш зручний спосіб роботи масивами в `php`. У дужках вказується ім'я масиву, потім після ключового слова `as` - пара змінних, розділених знаком `=>`, перша змінна для ключа масиву, друга - для значення в масиві за цим ключем. Перша змінна не є обов'язковою. Приклад:

```php
$a = range(1, 10);
foreach ($a as $key => $value) {
     echo $value . PHP_EOL;
}
````

Також є скорочений варіант циклу `foreach`, який застосовується у випадку, коли нам не потрібні ключі та цікавлять нас тільки значення масиву:

```php
$a = range(1, 10);
foreach ($a as $value) {
     echo $value . PHP_EOL;
}
````


## Константи

Якщо в програмі необхідно використовувати якесь число або рядок, і програміст знає, що цей рядок або число не змінюватимуться протягом роботи програми, найкраще використовувати константу.

```php
define("LOOP_LIMIT", 10);
define("LOOP_START", 1);
define("MESSAGE", 'Finish!');

$a = range(LOOP_START, LOOP_LIMIT);
foreach ($a as $key => $value) {
     echo $value . PHP_EOL;
}
echo MESSAGE;
````

## Домашка

[Домашнє завдання](hw5.md)
