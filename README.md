# Abhinav and Henry's Project

## Dataset

Microsoft Stock prices

## API Spec

Call: GET /price

Description: Gets all of MSFT's end of day prices.

Sample Output:


Call: GET /price/<day>

Description: Gets MSFT's end of day price for specified <day>

Sample Output:

Call: GET /average/<endDay>

Description: Gets MSFT's 10 day moving average of trading volume ending on <endDay>

Sample Output:


Call: POST /price/<day>

Description: Posts user's objects of prices to the day specified

Sample Output:


Call: GET /std

Description: Gets the standard deviation of MSFT end-of-day prices.

Sample Output:


## Usage

Curl: 

```curl -v http://localhost:8082/std```

Python:

```
import requests

resp = requests.get('http://localhost:8082/std')
if resp.status_code != 200:
    raise ApiError('GET /std/ {}'.format(resp.status_code))
print('Standard deviation: {}'.format(resp.json()))
```

## Pricing

$5 monthly for unlimited API access.

