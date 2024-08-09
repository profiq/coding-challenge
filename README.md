# Profiq Coding Challenge - Summer 2024 - CZ version

[Engish version](README-EN.md)

### Zadani
Napiš co nejkratší prompt, který vygeneruje kód implementující cache LRU v Typescriptu.
Prompt by měl vygenerovat třídu s názvem „LRUCache“ s odpovídajícím typem v TypeScriptu pro hodnotu našeho objektu.


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

Hondota by mela prijimat nasledujici objekt:
```
{ "users": [ { "id": 1, "name": "Alice", "email": "alice@example.com", "roles": ["admin", "editor"], "profile": { "age": 30, "address": { "street": "123 Main St", "city": "Wonderland", "postalCode": "12345" } } }, { "id": 2, "name": "Bob", "email": "bob@example.com", "roles": ["viewer"], "profile": { "age": 25, "address": { "street": "456 Side St", "city": "Underland", "postalCode": "67890" } } } ], "settings": { "theme": "dark", "notifications": { "email": true, "sms": false }, "privacy": { "trackLocation": false, "dataSharing": true } }, "metadata": { "version": "1.0.0", "timestamp": "2024-07-17T10:00:00Z" } }
```

Tvůj kód automaticky otestujeme na sadu standardních use casů, ale také na několik okrajových casů:

- metoda get() by měla vracet hodnotu “undefined”, pokud není klíč nalezen,
- metoda put() by měla přepsat předchozí hodnotu, pokud klíč již existuje,
- konstruktor by měl vyhodit řetězec „INCORRECT_CAPACITY“, pokud maxCapacity není v rozmemí 1 a 10000,
- metoda getMostRecentlyUsedKey() by měla vrátit hodnotu “undefined”, pokud ještě nebyl zpřístupněn žádný klíč nebo pokud je cache prázdná.

Kód vygenerovaný AI můžete otestovat v tomto projektu: https://replit.com/@PetrVecera/ai-challenge-2024#README.md

## Hodnoceni
Tvůj prompt otestujeme na gpt-3.5-turbo-0125 s teplotou nastavenou na 0 a max. počtem tokenů nastaveným na 4096 (všechny ostatní parametry budou mít výchozí hodnoty API).

### Bodovani
Nejprve seřadíme účastníky podle počtu úspěšně absolvovaných testů. Dále účastníky se stejným počtem absolvovaných test casů seřadíme podle délky "promptu" vyjádřené v počtemu vstupních tokenů.

V případě dotazů neváhejte vytvořit issue https://github.com/profiq/coding-challenge/issues.
