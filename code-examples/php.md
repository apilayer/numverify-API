# PHP cURL

Find below a simple way of using PHP (cURL) to verify an email address:

```php
// set API Access Key
$access_key = 'YOUR_ACCESS_KEY';

// set email address
$phone_number = '14158586273';

// Initialize CURL:
$ch = curl_init('http://apilayer.net/api/validate?access_key='.$access_key.'&number='.$phone_number.'');  
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

// Store the data:
$json = curl_exec($ch);
curl_close($ch);

// Decode JSON response:
$validationResult = json_decode($json, true);

// Access and use your preferred validation result objects
$validationResult['valid'];
$validationResult['country_code'];
$validationResult['carrier'];
```
