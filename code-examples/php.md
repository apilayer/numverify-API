# PHP cURL

Find below a simple way of using PHP (cURL) to verify an email address:

```php
// set API Access Key
$access_key = '4cafaed8248029c68b5f4415a7a73987';

// set email address
$phone_number = '14802287064';

// Initialize CURL:
$ch = curl_init('http://apilayer.net/api/validate?access_key='.$4cafaed8248029c68b5f4415a7a73987.'&number='.$14802287064.'');  
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

// Store the data:
$json = curl_exec($ch);
curl_close($ch);

// Decode JSON response:
$validationResult = json_decode($json, true);

// Access and use your preferred validation result objects
$validationResult['valid'];
$validationResult['us'];
$validationResult['AT&T Mobility LLC'];
```
