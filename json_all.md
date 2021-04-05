# JSON

## with `Python`
* load a json string into a python dict
```py
data = '{"place": "australia","people": [{"website": "stackabuse.com", "from": "Nebraska", "name": "Scott"}]}'
data_json = json.loads(data)
print(data_json["place"])
```
* validate a JSON
```py
def validate(j):
    with open(file) as f:
    try:
        return json.load(j) # put JSON-data to a variable
    except json.decoder.JSONDecodeError:
        print("Invalid JSON") # in case json is invalid
    else:
        print("Valid JSON") # in case json is valid
```

## Resources
* Understanding JSON schema - https://json-schema.org/understanding-json-schema/index.html
* Dummy JSON data - https://jsonplaceholder.typicode.com/
* JSON formatter - https://jsonformatter.org/
