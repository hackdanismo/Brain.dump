# Python

```python
import requests

# Page URL
url = "https://frontify.com/test"

try:
    # Use HEAD to avoid downloading the BODY
    response = requests.head(url, allow_redirects=True)

    # Return the status codes for the page URL provided
    if response.status_code == 200 or response.status_code == 404:
        print(f"{url}: {response.status_code}")
    else:
        print(f"{url}: {response.status_code}")

except requests.exceptions.RequestException as e:
    print(f"Error checking URL: {e}")
```
