# JSON

## with `Python`
* load a json string into a python dict
```py
data = '{"place": "australia","people": [{"website": "stackabuse.com", "from": "Nebraska", "name": "Scott"}]}'
data_json = json.loads(data)
print(data_json["place"])
```

## Resources
* Dummy JSON data - https://jsonplaceholder.typicode.com/
