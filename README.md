# CleverTap PHP Wrapper (unofficial)

Pushes events to your CleverTap account from your PHP application. An unofficial wrapper that uses the official API.

##Installation
Install using [Composer](https://getcomposer.org/)

    composer require xaneem/clevertap-php

##Sample code
Code for setting a profile and pushing an event. Please make sure you replace your Account ID and Passcode. It's available in Settings dashboard inside CleverTap.

    require_once "vendor/autoload.php";

    $clevertap = new \CleverTap\clevertap(
        'YOUR-ACCOUNT-ID', 
        'YOUR-PASSCODE'
    );

    // Setting profile and identity information
    print_r(
        $clevertap->setProfile(
        	'john@example.com',
        	[
        		'Name' => 'John Doe',
        		'Category' => 'Platinum'
        	]
        )
    );

    // Pushing an event
    print_r(
        $clevertap->pushEvent(
        	'Purchased product',
        	[
        		'Amount' => 2,
        		'Currency' => 'BTC'
        	]
        )
    );

## License
MIT License