visicalc
========

Google Spreadsheets API using Python

Installation
------------

`cd ~src/github`

`git clone git@github.com:davejagoda/visicalc.git`

`cd visicalc`

`virtualenv venv`

`source venv/bin/activate`

`pip install -r requirements.txt`

Setup
-----

You need a `client_secrets.json` file. Go here:

https://console.developers.google.com

Create a new project.

Create an OAuth2 client ID (type Other).

Save the JSON file somewhere safe.

Grant your project access:

`./writeGoogleBearerToken.py -c client_secrets.json -t oauth_token.json`

Resources
---------

http://www.payne.org/index.php/Reading_Google_Spreadsheets_in_Python

https://code.google.com/a/google.com/p/apps-api-issues/issues/detail?id=3851

Sample Invocations
------------------

Print out details about all your spreadsheets named 'foo' using your token:

`./lsSpreadsheet.py -t oauth_token.json -n foo`

Validate that dates are in ascending order:

`./validateSpreadsheet.py -t oauth_token.json -n foo -d`

Validate that numbers are in ascending order:

`./validateSpreadsheet.py -t oauth_token.json -n foo -i`
