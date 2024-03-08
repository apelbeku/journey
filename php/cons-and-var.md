# Constants And Variables

`Constant` are the value that cannot change once they are defined, unlike `Variable` where you could define and override the row variable after they are defined

```php
/**
 * The return is beku because last variable
 * Override the value.
 */
$firstname = "apel";
$firstname = "beku";

echo $firstname;
```

## How To Define Const

### Using `define()`

- Naming `const` follows the same rules as variables
- Use uppercase for `define('NAME', 'value')`
- When referenced a `const` you don't need `$`
- You can't change the value of a `const`

```php
define('NAME', 'value');
define('STATUS_PAID', 'paid');

echo STATUS_PAID;

/**
 * Check if the const is defined
 * use defined("NAME") function
 */
echo defined('STATUS_PAID');
```

### Using `const()`

Different between `const()` and `define()` is `const()` actually defined at compile time, while `define()` are defined at runtime. It means you can't use `const()` in control structure like `loop`/`if else`, but you can use `define()` in it

```php
/**
 * if(true) {
 *  define('STATUS_PAID', 'paid');
 * }
 const STATUS_PAID = 'paid';
 echo STATUS_PAID;
```

## When To Use `const()`

Whenever you have static data tha doesn't change too often, e.g:

- STATUS_PAID
- STATUS_VOID
- STATUS_PENDING
- STATUS_DECLINED

## Predefined `const`

`PHP` also have predefined and magic `const`

- [Predefined `const`](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbTdmVk95aXN4dmctZmJtazFGR0E0TUQyV1lUZ3xBQ3Jtc0treEpuMEZUYVNvSVgtMEFUb19NZDlucXlKS0J4TGhVeDFwa2YzME82OUxNdlBqcWVVRUstcXlCRUZkZkZfd01EY3plWVluMEo3T1R3VV9VLTd4SGFRZWlKX1hOSDQ3VzhBcGczVkRSem5vMS10SC0wSQ&q=https%3A%2F%2Fwww.php.net%2Fmanual%2Fen%2Freserved.constants.php&v=6JtP8xk1U_k)

```php
echo PHP_VERSION;
echo PHP_BINDIR;
echo PHP_BINARY;
echo PHP_CONFIG_FILE_PATH;
```
- [Magic `const`](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbVpmd0V1dzhJRkt6cVJHVVpobWwzSVdzRGh3Z3xBQ3Jtc0ttcDdBdHBlYzA5OWthMlZ3MUVfOGFNRVNCdjF6c3k0NzlaV0FYb2xUM2NYV3FpYTk3TGZKN2FoV2FOMUw2YUxNOVRzbG5oTFl0M2pUbEVWVnpTcFhJWXBxVFlyUXFXQVVMSlRRSFA3R05pRnVDWlA0RQ&q=https%3A%2F%2Fwww.php.net%2Fmanual%2Fen%2Flanguage.constants.magic.php&v=6JtP8xk1U_k)

```php
echo __LINE__;
echo __FILE__;
echo __FUNCTION__;
echo __METHOD__;
```

## Variable Variable

`Variable Variable` basically takes the value of the variable and treats that as the name of the new variable

```php
$foo = 'bar';
$$foo = 'baz';

echo $foo, $bar;

/**
 * Proper way to do it
 */
echo $foo, $$foo;
echo "$foo, ${$foo}";
echo "$foo, {$$foo}";
```
