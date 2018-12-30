# Attributes > Maps

***

> Read our article on [Maps](http://www.stencyl.com/help/view/maps/) for an explanation of these blocks.

***

## Create

### <a name="create-map"></a> Create New Map

![create new map](http://static.stencyl.com/pedia2/block-images/attributes/maps/create-map.png)

Creates a new, empty map. Usually, you'll assign it to a map attribute right away.

```
new Map<String, Dynamic>()
```

***

### <a name="copy-map"></a> Copy of Map

![copy of map](http://static.stencyl.com/pedia2/block-images/attributes/maps/copy-map.png)

Returns a shallow copy of the map.

```
Utils.copyMap(map)
```

***

## Modify

### <a name="set-map"></a> Set (Assign Key to Value)

![set key text to value object for map](http://static.stencyl.com/pedia2/block-images/attributes/maps/set-map.png)

Assigns the specified key to the given value for this map.

```
map.set([TEXT], [VALUE]);
```

***

### <a name="remove-map"></a> Remove Item (using Key)

![remove key text from map](http://static.stencyl.com/pedia2/block-images/attributes/maps/remove-map.png)

Removes the entry for the specified key from the map.

```
map.remove([TEXT]);
```

***

### <a name="empty-map"></a> Remove All Items

![remove all items from map](http://static.stencyl.com/pedia2/block-images/attributes/maps/empty-map.png)

Removes all entries from the map.

```
for(key in map.keys()) {
  map.remove(key);
}
```

***

## Access

### <a name="key-value"></a> Get (Value for Key)

![value of text for map](http://static.stencyl.com/pedia2/block-images/attributes/maps/key-value.png)

Returns the entry for the given key, or null if it doesn't exist.

```
map.get([TEXT])
```

***

### <a name="key-exists-map"></a> Map has Key?

![map has key text](http://static.stencyl.com/pedia2/block-images/attributes/maps/key-exists-map.png)

Returns `true` if an entry exists for the given key.

```
map.exists([TEXT])
```

***

### <a name="value-exists-map"></a> Map has Value?

![map has value object](http://static.stencyl.com/pedia2/block-images/attributes/maps/value-exists-map.png)

Returns `true` if the value exists in the map.

```
Utils.mapContainsValue(map, [VALUE])
```

***

### <a name="count-map"></a> Number of Items in Map

![number of items in map](http://static.stencyl.com/pedia2/block-images/attributes/maps/count-map.png)

Returns the number of entries in the map.

```
Utils.mapCount(map)
```

***

### <a name="map-is-empty"></a> Map is Empty?

![map is empty](http://static.stencyl.com/pedia2/block-images/attributes/maps/map-is-empty.png)

Returns `true` if the map contains no entries.

```
Utils.mapCount(map) == 0
```

***

### <a name="map-as-list"></a> Keys / Values of Map (as list)

![keys of map as list](http://static.stencyl.com/pedia2/block-images/attributes/maps/map-as-list.png)

Returns the `list` of [keys or values] for this map. No specific order is guaranteed. (In other words, do not count on it being the same order in which you added the entries.)

```
Utils.mapToList(map, "keys")
Utils.mapToList(map, "values")
```

***

### <a name="for-each-map"></a> For Each Item in Map ...

![for each key in map](http://static.stencyl.com/pedia2/block-images/attributes/maps/for-each-map.png)

Lets you perform logic on each item in the map. Use the embedded `item` block to retrieve the current item being examined.

```
//loop over keys
for(item in map.keys()) {
  [ACTION]
}

//loop over values
for(item in map) {
  [ACTION]
}
```

***
