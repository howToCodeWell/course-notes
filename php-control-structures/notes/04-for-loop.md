A for loop evaluates three expressions. 

On every iteration the second expression is re-evaluated until it resolves with a `false` outcome.

Once the second expression has resolved `ture` loop is completed.

The following is the structure of a PHP for loop
```php
for($expression1; $expression2; $expression3) {
    // Run statement(s)
}
```
The first expression is evaluated once at the beginning of the loop.

The second expression is evaluated per iteration. If the second expression resolves `true` then the statement(s) within the body of the for loop are executed.

If the second expression resolved `false` then the execution of the loop ends.

At the end of each iteration the third expression is evaluated.

The following is a real world example of how to use a for loop. 

In this example the `$discount` increases by `5` for every iteration of the loop.


```php
$discount = 0;
$productLimit = 3;
for ($basketQty = 1; $basketQty <= $productLimit; $basketQty++) {
    $discount = $discount + 5;
    echo 'Basket QTY is now '. $basketQty . "\n";
    echo 'Discount is now '. $discount . "\n";
}

// Basket QTY is now 1
// Discount is now 5
// Basket QTY is now 2
// Discount is now 10
// Basket QTY is now 3
// Discount is now 15
```

# Breaking the loop

When the conditional break statement is reached the loop no longer continues.

```php
for ($expression1; $expression2; $expression3) {
    if ($expression1 === 2) {
        break;
    }
}
```
In the below example the loop is broken when the `$discount` reaches the `$discountLimit`.
```php

$discount = 0;
$discountLimit = 20;
$productLimit = 10;

for ($basketQty = 1; $basketQty <= $productLimit; $basketQty++) {
    if ($discount === $discountLimit) {
        echo 'Discount limit reached' . "\n";
        break;
    }
    $discount = $discount + 5;
    echo 'Basket QTY is now '. $basketQty . "\n";
    echo 'Discount is now '. $discount . "\n";
}

// Basket QTY is now 1
// Discount is now 5
// Basket QTY is now 2
// Discount is now 10
// Basket QTY is now 3
// Discount is now 15
// Basket QTY is now 4
// Discount is now 20
// Discount limit reached
```


```php
$productsInBasket = [
    1, 1, 1, 1, 1, 1, 12, 15
];
$discount = 0;
$discountLimit = 20;
$productLimit = 10;
$productIDWithDiscount = 1;
$productLimit = 10;

for ($productIndex = 0; $productIndex <= $productLimit; $productIndex++) {
   
    if (!isset($productsInBasket[$productIndex])) {
        echo 'Product at index ' . $productIndex . ' Not found .... Loop completed '. "\n";
        break;
    }

    $currentProductID = $productsInBasket[$productIndex];
    
    if ($discount === $discountLimit) {
        echo 'Discount limit reached' . "\n";
        continue;
    }

    if ($productIDWithDiscount === $currentProductID) {
        $discount = $discount + 5;
    }    

    echo 'Discount is now '. $discount . "\n";
}

// Discount is now 5
// Discount is now 10
// Discount is now 15
Discount is now 20
Discount limit reached
Discount limit reached
Discount limit reached
Discount limit reached
Product at index 8 Not found .... Loop completed 


```