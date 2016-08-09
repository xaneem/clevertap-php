# CleverTap PHP Wrapper (unofficial)

Pushes events to your CleverTap account from your PHP application. An unofficial wrapper that uses the official API.

Install using composer.

Sample code to use this:

    require_once "vendor/autoload.php";

    $clevertap = new \CleverTap\clevertap(
        'TEST-XXX-XXX-XXXX', 
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
