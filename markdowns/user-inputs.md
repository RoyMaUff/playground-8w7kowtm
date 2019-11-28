# User Inputs

The script will need to read user inputs, and verify them before any processing.

You should never trust the user and implement a few ways to correct him of his mistake,
leading him to provide a correct guess.

**A mistake does not count as a try.**  

The script will read **strings only composed of 4 numbers, removing blanks or spaces.**

The codemaker will **analyse a limited amount** of codebreaker's guesses (10), providing either a win or a loose.  

_BONUS: You can implement a cheating word, resulting in an instant win, revealing the mystery code._  

## Hints

Here are some hints, but you really should try to find by yourself.

::: Click to see some hints

You can use iteration control structures such as:

- [for](https://www.php.net/manual/fr/control-structures.for.php)
- [while](https://www.php.net/manual/fr/control-structures.while.php)

You can use PHP built-in functions such as:

- [trim](https://www.php.net/manual/fr/function.trim.php)
- [strlen](https://www.php.net/manual/fr/function.strlen.php)
- [str_replace](https://www.php.net/manual/fr/function.str-replace.php)
- [fopen](https://www.php.net/manual/fr/function.fopen.php)
- [fgets](https://www.php.net/manual/fr/function.fgets.php)

:::

## Solution: Ask user for input

::: Click to see a way to read an user input

```php runnable
    write("Please guess a 4 digit number: ");
    $input = fopen("php://stdin", "r");
    $guess = fgets($input);
    $guess = trim($guess);
    $guess = str_replace(" ", "", $guess);
    var_dump($guess);
```

:::

::: Click to see a way to do something multiple times

```php runnable
    $tries = 0;
    while($tries < 10){
        \echo ++$tries . PHP_EOL;
    }
```

:::
