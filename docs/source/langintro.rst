Вступ до мови
================================

Мова програмування, яка використовується в компіляторі, розроблена спеціально для нього і містить обмежену кількість конструкцій, які транслюються в асемблерні коди.

Присвоєння
------------------------------------
Для того, щоб присвоїти значення змінній достатньо написати ім'я цієї змінної на початку рядка, знак дорівнює "=" та значення::
	
	x = 5;

Також можна присвоювати значення будь-якого математичного виразу::

	x = (a+b)*10;

Допустимі операції:
	
	#) Додавання, віднімання "+", "-"
	#) Множення, цілочислене ділення "*", "/"
	#) Остача від ділення: "%"


Оператор розгалуження
------------------------------------
Конструкція розгалуження має вигляд::

	if <вираз>:
		<блок операторів 1>
	else:
		<блок операторів 2>
	endif;

Якщо результат виразу є істиною, то буде виконаний блок операторів 1, інакше - блок операторів 2.

У виразі можуть бути використані математичні операції, а також такі оператори як ">", "<", ">=", "<=", "=".


Оголошення змінних
------------------------------------

В мові немає особливих конструкцій для оголошення змінних. Всі змінні, які були використані у програмі в будь-якому місці вважаються оголошеними.

Тип усіх змінних є цілочисленим подвійним словом.

Всі змінні, використані у функціях є локальними. Для роботи з зовнішніми змінними можна використовувати лише параметри функції. Змінні передаються за значенням.


Оголошення функцій
------------------------------------
Для оголошення функції використовується ключове слово "function". Синтаксис оголошення є таким::

	function <name>(<аргументи, розділені комою>)
		<блок операторів>
		return <змінна>;
	endfunc;

Інтерактивна консоль
------------------------------------

Друк на екран
^^^^^^^^^^^^^^^^^^^^^^^^^^
Для друку на екран використовується оператор "print". Оператор існує в двох формах:

	1) друк змінної ::

	print var;
	
	2) друк строкового літералу ::

	print "Hello, world";

В рядках може бути символи "\\n", які автоматично замінюються на символи переводу рядка.


Зчитування з клавіатури
^^^^^^^^^^^^^^^^^^^^^^^^^^
Для читання з клавіатури використовується оператор "read".

Наприклад, читання числа з клавіатури::
	
	read var;

Оператори циклу
-----------------------------------
В мові існує оператор циклу while, який реалізує цикл з передумовою. Синтаксис оператору::

	while <умова повтору>:
		<блок операторів>
	endwhile;

За умови істиності умови повтору, програма буде повторювати блок операторів.

За допомогою цієї конструкції легко реалізувати повторення блоку задану кількість разів::

	N = 1;
	while N<=4:
		print N;
		print "\n";
		N = N+1;
	endwhile;

В даному випадку цикл буде виконуватись 4 рази, друкуючи кожну ітерацію лічильник. Вивод буде таким::

	1
	2
	3
	4


Висновки
------------------------------------
Розроблена мова програмування є повною за Тюрингом, тобто за допомогою неї можна обчислити будь-яку математичну функцію.