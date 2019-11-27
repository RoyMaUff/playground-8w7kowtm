# A Solution

Source code of the demo.

<details>
    <summary>Click to see the source code</summary>

    ```php runnable
        function write(string $message)
        {
            \fwrite(STDOUT, $message . PHP_EOL);
        }

        $n1 = \random_int(0, 9);
        $n2 = \random_int(0, 9);
        $n3 = \random_int(0, 9);
        $n4 = \random_int(0, 9);
        $mysteryArray = [$n1, $n2, $n3, $n4];
        $mystery = \implode($mysteryArray);
        $guess = null;
        $tries = 0;

        write("MASTERMIND");

        // While guess is wrong and number of tries not reached
        while ($guess != $mystery && $tries < 10) {
            // Prompt to User his guess
            if ($tries > 0) {
                write("You guessed: $guess");
            }

            // Read user input
            write("Please guess a 4 digit number: ");
            $input = \fopen("php://stdin", "r");
            $guess = \fgets($input);
            $guess = \trim($guess);
            $guess = \str_replace(" ", "", $guess);

            // CHEAT
            if ($guess === "CHEAT") {
                write("GG YOU WON!   ...cheater...");
                write("The mystery number was $mystery!");
                exit();
            }

            // Validate user input
            if (!\is_numeric($guess)) {
                write("You need to enter numbers...");
                continue;
            }
            if (\strlen($guess) !== 4) {
                write("You need to enter 4 numbers...");
                continue;
            }

            // Incrementing tries
            ++$tries;

            // Clues for user
            write("Sorry that is not the mystery number");
            $guessArray = \str_split($guess);
            foreach ($guessArray as $index => $proposal) {
                if ($mysteryArray[$index] == $proposal) {
                    write("{$proposal} is in the right spot!");
                } elseif (\in_array($proposal, $mysteryArray)) {
                    write("{$proposal} is in the number");
                }
            }
        }

        if ($tries === 10) {
            write("$tries tries reached, sorry you loose! :(");
            write("The mystery number was $mystery");
            exit();
        }

        write("OMG, GG you guessed it! :D");
    ```
</details>
