# Time Traveling Key Value store

Design a time-based key-value data structure that can store multiple values for the same key at different time stamps and retrieve the key's value at a certain timestamp.

## Implement the `TimeMap` class:

* `void set(String key, String value, int timestamp)`
  * Stores the key key with the value value at the given time timestamp.

* `String get(String key, int timestamp)`
  * Returns a value such that set was called previously, with `timestamp_prev <= timestamp`. If there are multiple such values, it returns the value associated with the largest timestamp_prev. If there are no values, it returns "".

## Examples

```javascript
timeMap.set('foo', 'bar', 1);
timeMap.get('foo', 1); //returns 'bar'
timeMap.get('foo', 3); //returns 'bar'
timeMap.set('foo', 'baz', 3);
timeMap.get('foo', 1); // returns 'bar'
timeMap.get('foo', 2); // returns 'bar'
timeMap.get('foo', 3); // returns 'baz'
```

## Constraints

* key and value are strings
* The `timestamp` given in `set` are strictly increasing.
