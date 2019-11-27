# Dialog

A program can not be executed without providing some informations to the user.

An elegant way to do it would be to use a function taking a message as parameter,
displaying it to the user with some formatting.

Here are some hints, but you really should try to find by yourself.
<details>
    <summary>Click to see some hints</summary>

    To display some informations, you can use PHP built-in functions such as:

    - [fwrite](https://www.php.net/manual/fr/function.fwrite.php)
    - [echo](https://www.php.net/manual/fr/function.echo.php)
    - [print](https://www.php.net/manual/fr/function.print.php)

</details>

Solution:
<details>
    <summary>Click to see a way to implement it</summary>

    ```php runnable
        function write(string $message)
        {
            \fwrite(STDOUT, $message . PHP_EOL);
        }
        \write("I am a first sentence.");
        \write("I am a second sentence.");
    ```
</details>
