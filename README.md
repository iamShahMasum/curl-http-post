# curl-http-post
PHP curl + http POST


<?php

// create curl object
$curl = new CurlPost('http://www.example.com');

try {
	// execute the request
	echo $curl([
		'username' => 'user1',
		'password' => 'passuser1',
		'gender'   => 1,
	]);
} catch (\RuntimeException $ex) {
	// catch errors
	die(sprintf('Http error %s with code %d', $ex->getMessage(), $ex->getCode()));
}
