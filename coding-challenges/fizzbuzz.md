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
/**
 * Get the FizzBuzz result
 * @param integer $n - total number requested
 * @return  string - the fizzbuzz result
 */
function fizzOrBuz( $n ) {
    $fizzbuzz = '';

    for( $i = 1; $i <= $n; $i ++ ) {
        $output = '';

        if ( $i % 3 == 0 ) $output = 'Fizz';
        if ( $i % 5 == 0 ) $output .= 'Buzz';

        $fizzbuzz .= (( empty( $output ) ) ? $i : $output ) . '<br />';
    }
    return $fizzbuzz;
}

echo fizzOrBuz(100);
```

**Working example**

http://alexandrecanijo.com/challenges/fizzbuzz.php


