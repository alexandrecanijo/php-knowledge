### FizzBuzz

The rules of FizzBuzz are as follows:

* For numbers 1 through 100,
  * if the number is divisible by 3 print Fizz;
  * if the number is divisible by 5 print Buzz;
  * if the number is divisible by 3 and 5 \(15\) print FizzBuzz;
  * else, print the number.

There are several ways to approach this challenge.

The one that I like the most, since it's more readable is this:

```php
for( $i = 1; $i <= 100; $i ++ )
{
    $output = '';

    if ( $i % 3 == 0 ) $output = 'Fizz';
    if ( $i % 5 == 0 ) $output .= 'Buzz';

    echo ( empty( $output ) ) ? $i : $output;
    echo '<br />\n';
}
```


<iframe width="560" height="315" src="https://php-knowledge-alexandrecanijo.codeanyapp.com/challenges/fizzbuzz.php" frameborder="0" allowfullscreen></iframe>



