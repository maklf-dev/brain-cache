
# JSON

## What is JSON
a text that represents data; a data message.

**JavaScript Object:**
```
var user = [
    name: "Json",
    age: -13
];
```

**JSON:**
```
{
    "name": "Json",
    "age": -13
}
```
- *JavaScript Object* is data inside JS memory, but *JSON* is a text format to **store** or **transform** data.
- **Note** that in JSON, keys need double quotes but in js object, they don't.

## Usage

1. APIs
2. localStorage
3. Form data
4. Dynamic UI rendering
5. Configuration files
6. Translations

## Syntax Validation

| Type | Example |
| --- | --- |
| String | "float" | 
| Number | 0 |
| Boolean | true - false |
| Null | null |
| Array | ["arr", "ay"] |
| Object | {"int" : 0.2} |

> so *undefined*, *function() {}*, *new Date()* ,... is not valid in JSON.

### Valid Example:

```
{
  "id": 1,
  "title": "Gold Ring",
  "price": 450,
  "available": true,
  "tags": ["jewelry", "gold"],
  "details": {
    "weight": 3.5,
    "unit": "gram"
  },
  "discount": null
}
```