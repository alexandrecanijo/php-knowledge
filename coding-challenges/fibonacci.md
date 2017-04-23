### Fibonacci

The Fibonacci sequence is a series of numbers where a number is found by adding up the two numbers before it.
Starting with 0 and 1, the sequence goes:

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, and so forth.

Here is one of the many solutions for this challenge:

```php
/**
 * Get the Fibonacci Number, using a recursive function
 * @param integer $n - number to check
 * @return integer - the resulting number of the calculation
 */
function getFibonacciNumber( $n ) {
    if (( $n == 0 ) || ( $n == 1 )) {
        return $n;
    }
    return getFibonacciNumber( $n - 2 ) + getFibonacciNumber( $n - 1 );
}

/**
 * Get Fibonacci series, depending on how many values we want
 * @param integer $n - series length
 * @return  string - the fibonacci series
 */
function getFibonacciSeries( $n ) {
    $series = '';
    for($i = 0; $i <= $n; $i++) {
        $series .= ( $i === $n) ? getFibonacciNumber($i) : getFibonacciNumber($i) . ', ';
    }
    return $series;
}

// Now, just get a series of 20 Fibonacci numbers
echo getFibonacciSeries(20);
```

**Working example**

http://alexandrecanijo.com/challenges/fibonacci.php





