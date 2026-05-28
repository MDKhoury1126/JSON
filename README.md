```# JSON
import urllib.request
import json

url = input('Enter URL: ')
data = urllib.request.urlopen(url).read().decode()
# decode turns bytes into strings
info = json.loads(data)
# info is a Python dictionary that contains the data from the JSON document. The json.loads() function takes a JSON-formatted string and converts it into a Python object, which in this case is a dictionary. This allows us to access the data in the JSON document using Python's dictionary syntax.

Total = 0
for item in info['comments']:
    Total += int(item['count'])
    print('Sum:', Total)```
