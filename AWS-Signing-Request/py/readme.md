## Description

Use this python script to make a get request to the License Validatoin API. Script include formatting and submission of AWS signature request, as well as API key.

## Requirements 

* API Key provided by Mass Data Office to state entities and municipalities

* AWS IAM user access credentials provided by Mass Data Office to 3rd party application developers and vendors
 * Access Key
 * Secret Key
 
* Python 2.0 or later

## Installation

```

 pip requests

```

## Usage

```

 python awsSigning.py
 
```

## Code modifications

Edit this code segment to modify the request and include the API key:

```

# ************* REQUEST VALUES *************
request_id = '<Enter License Number>'
method = 'GET'
service = 'execute-api'
host = '4bqnosml1f.execute-api.us-east-1.amazonaws.com'
region = 'us-east-1'
endpoint = 'https://4bqnosml1f.execute-api.us-east-1.amazonaws.com/alpha/v1/licenses/'+request_id
request_parameters = ''
apikey = '<Enter API Key>'
 
```

Edit this code segment to include your AWS credentials (Best practices would be to use enviroment variable for the access key and secret key):

```

# Read AWS access key from env. variables or configuration file. Best practice is NOT
# to embed credentials in code.
access_key = os.environ.get('AWS_ACCESS_KEY_ID')
secret_key = os.environ.get('AWS_SECRET_ACCESS_KEY')

 
```


