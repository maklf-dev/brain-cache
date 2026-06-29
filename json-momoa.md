
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
- **Note** that in JSON, keys are *string* and need double quotes but in js object, they're not.

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

## Working With JSON

- read it
- loop it
- search it
- add/update/delete it
- transform it
- render it
- save it
- load it
- send it to server
- receive it from server

## Randoms

- almost all programming languages has some form of library or built-in functionality to parse JSON

## JSON in JS

> [Function and helpers for JSON in JS](json-momoa_funcs.md)

## Sorces
- [**📺 Learn JSON in 10 Minutes - Web Dev Simplified**](https://www.youtube.com/watch?v=iiADhChRriM)
- [**🧠 AI**](https://chatgpt.com/)