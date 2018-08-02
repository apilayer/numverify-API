# jQuery.ajax

Find below a simple way of using jQuery.ajax to validate any phone number:

```javascript
// set endpoint and your access key
var access_key = 'YOUR_ACCESS_KEY';
var phone_number = '14158586273';

// verify phone number via AJAX call
$.ajax({
    url: 'http://apilayer.net/api/validate?access_key=' + access_key + '&number=' + phone_number,   
    dataType: 'jsonp',
    success: function(json) {

    // Access and use your preferred validation result objects
    console.log(json.valid);
    console.log(json.country_code);
    console.log(json.carrier);
                
    }
});
```
  
