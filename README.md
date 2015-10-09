# shopperapproved-reviews-page
Generates review page for shopper approved reviews from api

1. Create a cms page for your reviews and this to your CMS page content:

```html
<h2>My Site is Shopper Approved</h2>
<h3>See a Few of Our Reviews Below</h3>
{{block type="core/template" template="customer_reviews/reviews.phtml"}}
```

2. You must insert your SITEID from shopper approved into the reviews.phtml in two places where it says MYSITEID
