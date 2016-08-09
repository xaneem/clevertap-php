# CleverTap PHP Wrapper (unofficial)

Pushes events to your CleverTap account from your PHP application. An unofficial wrapper that uses the official API.

##Installation
Install using [Composer](https://getcomposer.org/)

    composer require xaneem/clevertap-php

##Sample code
Code for setting a profile and pushing an event. Make sure you replace youe

    require_once "vendor/autoload.php";

    $clevertap = new \CleverTap\clevertap(
        'XXX-XXX-XXXX', 
        'XXX-XXX-XXXX');

    // Setting Profile
    print_r($clevertap->setProfile(
    	'john@example.com',
    	[
    		'Name' => 'John Doe',
    		'Category' => 'Platinum'
    	]
    ));

    // Creating Event
    print_r($clevertap->pushEvent(
    	'Purchased product',
    	[
    		'Amount' => 2,
    		'Currency' => 'BTC'
    	]
    ));

## License
MIT License