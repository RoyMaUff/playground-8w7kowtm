# Random Numbers

As the games rules states, we will need to generate random numbers.

**You can only use zero or positive integer between 1 and 9.**  

Here are some hints, but you really should try to find by yourself.

## Hints

::: Click to see some hints

To generate random numbers, you can use PHP built-in functions such as:

- [rand](https://www.php.net/manual/fr/function.rand.php)
- [random_int](https://www.php.net/manual/fr/function.random-int.php)

It is easier to use `random_int`.

:::

## Solution

::: Click to see a way to generate random numbers

```php runnable
    $n1 = random_int(0, 9);
    var_dump($n1);
```

:::
