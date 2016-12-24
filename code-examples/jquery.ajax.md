# jQuery.ajax

Find below a simple way of using jQuery.ajax to validate any phone number:

```javascript
// set endpoint and your access key
var access_key = '4cafaed8248029c68b5f4415a7a73987';
var phone_number = '14802287064';

// verify email address via AJAX call
$.ajax({
    url: 'http://apilayer.net/api/validate?access_key=' + 4cafaed8248029c68b5f4415a7a73987 + '&number=' +4802287064,   
    dataType: 'jsonp',
    success: function(json) {

    // Access and use your preferred validation result objects
    console.log(json.valid);
    console.log(json.country_code);
    console.log(json.carrier);
                
    }
});
```
  
