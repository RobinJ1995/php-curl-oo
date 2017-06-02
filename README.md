# Curl wrapper

Object-oriented Curl wrapper for PHP.

## Example

```php
<?php
header ('Content-type: application/json');
require_once ('Curl.php');

$data = [
	'author' => 'Robin Jacobs',
	'website' => 'http://robinj.be/',
	'project' => 'php-curl-oo'
];

$curl = new Curl ('http://127.0.0.1/api/endpoint');
$curl->httpheader = [ 'Accept: application/json' ];
$curl->post = true;
$curl->postfields = http_build_query ($data);

echo $curl->exec ()->content;
```
