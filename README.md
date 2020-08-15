# CliTextHandler
A simple php class to colorize Php-cli and work with

## Features
* Add color mark to text to colorize rest of text using `CliTextHandler::set_color_`[COLOR](#colors-list):
``` php
<?php
use realSamy\Tools\CliTextHandler;

include 'CliTextHandler.php';

echo 'This is a normal text! ' . CliTextHandler::set_color_green() . 'But this is green text!' . PHP_EOL;
echo 'This is still a green text! ' .  CliTextHandler::set_color_reset() . 'Now this is a normal text!';
```

* Colorize a part of text using `CliTextHandler::echo_`[COLOR](#colors-list):
``` php
<?php
use realSamy\Tools\CliTextHandler;

include 'CliTextHandler.php';

echo CliTextHandler::echo_cyan('This is a cyan text!') . ' But this is a normal text!';
```

* Change cursor position:
``` php
<?php
use realSamy\Tools\CliTextHandler;

include 'CliTextHandler.php';

echo CliTextHandler::down(3) . CliTextHandler::right(4) . ' This text started at 4 column right and 3 rows down!';
```

* Get values from cli with a given length:
``` php
<?php
use realSamy\Tools\CliTextHandler;

include 'CliTextHandler.php';

$answer = CliTextHandler::readline('Put 5 letters here: %s, just 5 letters please!', 5, true); //using true as last parameter makes you sure just given length will be accepted! otherwise if you don't need user answer as length as you define, let the last parameter empty.
echo 'Your answer was: ' . $answer;
```

## Colors list:
**Color**|**Light Color**
:-----:|:-----:
black| light\_black
red| light\_red
green| light\_green
yellow| light\_yellow
blue| light\_blue
purple| light\_purple
cyan| light\_cyan
white| light\_white
