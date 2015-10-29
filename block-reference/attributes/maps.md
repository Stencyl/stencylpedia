# Attributes > Maps

***

> Read our article on [Maps](http://www.stencyl.com/help/view/maps/) for an explanation of these blocks.

***

## Modify

### Set (Assign Key to Value)

![set-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/set-map.png)

Assigns the specified key to the given value for this map.

```
map.set([TEXT], [VALUE]);
```

***

### Remove Item (using Key)

![remove-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/remove-map.png)

Removes the entry for the specified key from the map.

```
map.remove([TEXT]);
```

***

### Remove All Items

![empty-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/empty-map.png)

Removes all entries from the map.

```
for(key in map.keys()) {
	map.remove(key);
}
```

***

## Getters

### Get (Value for Key)

![get-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/key-value.png)

Returns the entry for the given key, or null if it doesn't exist.

```
map.get("text")
```

***

### Map has Key?

![key-exists-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/key-exists-map.png)

Returns `true` if an entry exists for the given key.

```
map.exists([TEXT])
```

***

### Map has Value?

![value-exists-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/value-exists-map.png)

Returns `true` if the value exists in the map.

```
Utils.mapContainsValue(map, [VALUE])
```

***

### Number of Items in Map

![size-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/count-map.png)

Returns the number of entries in the map.

```
Utils.mapCount(map)
```

***

### Map is Empty?

![is-empty-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/map-is-empty.png)

Returns `true` if the map contains no entries.

```
Utils.mapCount(map) == 0
```

***

### Keys of Map (as list)

![list-keys-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/map-as-list.png)

Returns the `list` of keys for this map. No specific order is guaranteed. (In other words, do not count on it being the same order in which you added the keys.)

```
Utils.mapToList(map, "keys")
```

***

## Create / Copy

### Create New Map

![create-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/create-map.png)

Creates a new, empty map. Usually, you'll assign it to a map attribute right away.

```
new Map<String, Dynamic>()
```

***

### Copy of Map

![copy-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/copy-map.png)

Returns a shallow copy of the map.

```
Utils.copyMap(map)
```

***

## Looping

### For Each Item in Map...

![for-each-map-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/4%20-%20Maps/for-each-map.png)

Lets you perform logic on each item in the map. Use the embedded `item` block to retrieve the current item being examined.

```
for(item in map.keys()) {
	[ACTION]
}
```

***
