# Halfords Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Halfords Scraper](https://oxylabs.io/products/scraper-api/ecommerce/halfords?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Halfords website effortlessly. This brief guide showcases how Halfords Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Halfords results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Halfords page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.halfords.com/bikes/mountain-bikes/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/halfords-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n\n\n\n<!DOCTYPE html>\n<html xmlns=\"http://www.w3.org/1999/xhtml\" lang=\"en\" xml:lang=\"en\" prefix=\"og: h ... </html>",
      "created_at": "2024-02-20 12:38:02",
      "updated_at": "2024-02-20 12:38:06",
      "page": 1,
      "url": "https://www.halfords.com/bikes/mountain-bikes/",
      "job_id": "7165686035999923201",
      "status_code": 200
    }
  ]
}
```
With our Halfords Scraper, you can smoothly gather the necessary public data from any Halfords web page. Be it product-specific details including its pricing, customer opinions, or detailed descriptions - you can receive it all for market analysis or competitive advantage. If you need any assistance, our support team is readily available via live chat, or you can reach out to us at hello@oxylabs.io.