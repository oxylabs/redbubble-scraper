# Redbubble Scraper API

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.io/pages/gitoxy?utm_source=877&utm_medium=affiliate&groupid=877&utm_content=redbubble-scraper-github&transaction_id=102f49063ab94276ae8f116d224b67)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs' [Redbubble Scraper](https://oxylabs.io/products/scraper-api/ecommerce/redbubble?utm_source=github&utm_medium=repositories&utm_campaign=product) (a part of Web Scraper API) is a data gathering solution allowing you to extract real-time information from an Redbubble website effortlessly. This brief guide showcases how Redbubble Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Redbubble results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Redbubble page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.redbubble.com/g/t-shirts'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/redbubble-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><title data-react-helmet=\"true\">T-Shirts for Sale | Redbubble</ ... </html>",
      "created_at": "2024-02-20 12:32:00",
      "updated_at": "2024-02-20 12:32:06",
      "page": 1,
      "url": "https://www.redbubble.com/g/t-shirts",
      "job_id": "7165684517376645121",
      "status_code": 200
    }
  ]
}
```
With our Redbubble Scraper, you can seamlessly extract public data from any of your targeted Redbubble web pages. Gather the necessary artwork details, such as artist name, medium, price, and reviews. Use these insights to understand market trends and maintain a competitive edge. If you need any assistance, our support team is readily available through live chat or you can email us at hello@oxylabs.io.
