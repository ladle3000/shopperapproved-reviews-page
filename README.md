<span style="font-color:red;">This is probably completely irrelevant since approx 2020 since shopper approved now can do this out of the box.</span>

# Shopper Approved Reviews Page for Magento
#### Also adds schema for overall star ratings for your results in google etc.
Generates review page for shopper approved reviews from the Shopper Approved API.  You need a valid shopper approved account with active reviews.  Visit advanced tools>API in your shopper approved account and enter your name in the API section to get access.  Within this you will find your SITEID which you will need for this project.

<strong>Important:</strong> Please follow directions below for installation.

1.) Create a cms page for your reviews and this to your CMS page content:

```html
<h2>My Site is Shopper Approved</h2>
<h3>See a Few of Our Reviews Below</h3>
{{block type="core/template" template="customer_reviews/reviews.phtml"}}
```

2.) You must insert your SITEID from shopper approved into the reviews.phtml in two places where it says YOURSITEID

```php
$reviews = simplexml_load_file("https://www.shopperapproved.com/api/xml/reviews/?siteid=YOURSITEID&token=j6ZQGKY7C0m25sT&from=2014-01-01&to=$date&sort=newest&page=0");
```
and
```php
echo file_get_contents('https://www.shopperapproved.com/feeds/schema.php/?siteid=YOURSITEID&token=j6ZQGKY7C0m25sT');
```
