# Profiq Coding Challenge - Summer 2024

### Assigment
Write the shortest possible prompt that generates a code implementing an LRU cache in Typescript. 
The prompt should generate a class named “LRUCache” with corresponding TypeScript type for the input value.

```javascript
export class LRUCache {
  constructor(maxCapacity: int) {
             		…
  }
  
  put(key: string, value: ValueObject) {
  	…
  }
  
  get(key: string): ValueObject {
  	…
  }
  
  getMostRecentlyUsedKey(): ValueObject {
  	…
  }
}
```

The value should accept following object:
```
{ "users": [ { "id": 1, "name": "Alice", "email": "alice@example.com", "roles": ["admin", "editor"], "profile": { "age": 30, "address": { "street": "123 Main St", "city": "Wonderland", "postalCode": "12345" } } }, { "id": 2, "name": "Bob", "email": "bob@example.com", "roles": ["viewer"], "profile": { "age": 25, "address": { "street": "456 Side St", "city": "Underland", "postalCode": "67890" } } } ], "settings": { "theme": "dark", "notifications": { "email": true, "sms": false }, "privacy": { "trackLocation": false, "dataSharing": true } }, "metadata": { "version": "1.0.0", "timestamp": "2024-07-17T10:00:00Z" } }
```

Your code will be tested automatically against a set of standard use cases, but also against a few edge cases:
- get() should return undefined if the key is not found
- put() should override the previous value if the key already exists
- constructor should throw a string “INCORRECT_CAPACITY” if maxCapacity is not between 1 and 10000
- getMostRecentlyUsedKey() should return undefined if no key was accessed yet or if the cache is empty

You can test your AI generated code in this project 
https://replit.com/@PetrVecera/ai-challenge-2024#README.md

## Evaluation
Your prompt will be tested on gpt-3.5-turbo-0125 with temperature set to 0 and max tokens set to 4096 (all other parameters will have default API values). The tests will be as shown in the Replit

### Scoring:
- First, we will rank participants according to the number of test cases passed
- Then, participants with the same number of test cases passed will be ranked by prompt length in number of input tokens.

In case of questions, feel free to create an issue https://github.com/profiq/coding-challenge/issues
