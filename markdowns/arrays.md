# Ordered list

The codemaker must generate a four digit code, keeping the order of digit.
It will be convenient to find a programming structure which can do so.

## Hints

Here are some hints, but you really should try to find by yourself.
::: Click to see some hints

    To store ordered list of string, items, or number, you can use PHP associative arrays:

    - [array](https://www.php.net/manual/fr/function.array.php)
    - [implode](https://www.php.net/manual/fr/function.implode.php)
    - [str_split](https://www.php.net/manual/fr/function.str-split.php)

:::

## Solution

::: Click to see a way to implement it

```php runnable
    $mysteryArray = [4, 1, 3, 2];
    \var_dump($mysteryArray);
```

```php runnable
    $mysteryString = \implode([1, 2, 3, 4]);
    \var_dump($mysteryString);
```

```php runnable
    $newMysteryArray = \str_split("1234");
    \var_dump($newMysteryArray);
```

:::
