# Basic PHP Syntax

Default `APACHE` web directory is located in `/var/www/html`. And if you want your file to be interpreted as `php`, make sure it ends with `.php`. The `PHP` files can also have `HTML`, `CSS` and even `JavaScript` within them. So it would work pretty much the same way.

## Basic Syntax

The way `PHP` is parsed is that it looks for the opening and closing tags and interprets everything in between as `PHP`.

```php
<?php
Anything in between this code block will be interpreted as php
?>
```

If your file entirely contains `PHP` you don't need the closing tag and in fact should not have the closing tag. That's to ensure your website isn't messed up by unintentional white space or new lines introduced after the `PHP` closing tag

```php
<?php
```

## Hello World!

This is how you 'print' `Hello World!`

```php
<?php echo 'Hello World!'; ?>
```

## Run PHP In Terminal

```sh
php <file.php>
```

## Print VS Echo

Another way to `print` something:

- Use `print`
    ```php
    <?php print 'Hello World!'
    ```
    - `print` has return value of 1
    - You can `echo print`
    ```php
    <?php echo print 'Hello World' # And you will still get Hello World!1
    ```
    - `print` could be use within expression while `echo` cann't
    - Another way to `print`
    ```php
    <?php print('Hello World!')
    ```
- use `echo`
    ```php
    <?php echo 'Hello World!'
    ```
    - You cann't `print echo`, you will get parser error
    - Another way to `echo`
    ```php
    <?= 'Hello', . ,'World!'
    ```
    - If you use this you cann't concatenate
    ```php
    <?php echo('Hello World!')
    ```
    - Also `echo` is marginally faster than `print`, so i woul d suggest to use `echo` unless you have a specific reason to use `print`

## Escaping Quotes

- Use double quote
```php
<?= "joe's Invoice"
```
- Use backslash
```php
<?= 'Joe\'s Invoice'
```
- Recommended using double quote

## Variables

A few rules when creating variable in `PHP`

- Must start with a letter or an underscore
```php
$name/$_name
```
- The letter can be uppercase or lowercase
```php
$NAME/$name
```
- Don't start with number or a special character
```php
$1name/$@name
```
- Don't use `$this`. because it's refer to object
```php
$this
```

By default in `PHP` variables are assigned by value

```php
$x = 1;
$y = $X;
# you will get 1 becuase it's assigned by value, if you want $y change whenever $x change you should write like this

$x = 1;
$y = &$x;

$x = 4;
echo $y;
```

### Variable Within Text

```php
$firstname = 'apel';

echo 'Hello $firstname';
```

If you want to get value from the variable you need to change from single quote to double quote

```php
$firstname = 'apel';

echo "Hello $firstname";
# some developer will write like this
echo "Hello {$firstname}";
# or
echo "Hello" . $firstname;
```

## PHP In HTML

How to embed `PHP` in `HTML`

```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>
<h1><?= 'Hello World!' ?></h1>
<p>shorthand version of echo</p>
<p> You should use this if you just need print something</p>
<h1>
    <?php
        $x = 10;
        $y = 9;

        echo $x . ', ' . $y;
        # Or we can print content within a paragraph for example

        echo <p> $x . ', ' . $y; </p>

        # This is good for dynamically html generate but in general i would say that's not good idea to mix HTML directly in you PHP
    ?>
</h1>
</body>
</html>
```

## Comments

Several way to comment in `PHP`

- Single line comment
    - double slash `//`
    - hash `#`
    ```php
    // Using double slash
    # Using hash
    ```
- Multiline comment
    - multiline
    ```php
    /* 
        This is multiline comment
     */
    ```
    - doc log comment
    ```php
    /**
     * This is doc log comment
     * for write documentation
     * about your source code.
     */
    ```
