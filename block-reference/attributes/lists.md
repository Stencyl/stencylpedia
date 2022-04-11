# Attributes > Lists

***

> Read our article on [Lists](https://www.stencyl.com/help/view/lists/) for an explanation of these blocks.

***

## Create

### <a name="create-list"></a> Create New List

![create new list](https://static.stencyl.com/pedia2/block-images/attributes/lists/create-list.png)

Creates and returns an empty list. Usually, you'll want to set this immediately to a list attribute.

```
new Array<Dynamic>()
```

***

### <a name="copy-list"></a> Copy of List

![copy of list](https://static.stencyl.com/pedia2/block-images/attributes/lists/copy-list.png)

Returns a shallow copy of the specified list.

```
list.copy()
```

***

## Add / Insert

### <a name="add-list"></a> Add Item to List

![add object to list](https://static.stencyl.com/pedia2/block-images/attributes/lists/add-list.png)

Adds the given value to the end of the list.

```
list.push([VALUE]);
```

***

### <a name="insert-list"></a> Insert Item into List

![insert object at int to list](https://static.stencyl.com/pedia2/block-images/attributes/lists/insert-list.png)

Inserts the given value at the specified index of the list. This will push everything at that index and after down one position. The index must be between 0 and (size of list - 1) inclusive.

```
list.insert([INT], [VALUE]);
```

***

## Remove / Replace

### <a name="remove-item"></a> Remove Item from List

![remove object from list](https://static.stencyl.com/pedia2/block-images/attributes/lists/remove-item.png)

Removes the given value from the list, if it exists. If it does not exist, nothing happens.

```
list.remove([VALUE]);
```

***

### <a name="remove-index"></a> Remove Item from Index

![remove item # int from list](https://static.stencyl.com/pedia2/block-images/attributes/lists/remove-index.png)

Removes the value at the specified index from the list. The index must be between 0 and (size of list - 1) inclusive.

```
list.splice([INT], 1);
```

***

### <a name="replace-list"></a> Replace Item in List

![replace item # int with object in list](https://static.stencyl.com/pedia2/block-images/attributes/lists/replace-list.png)

Replaces the item at the specified index with another for the list. The index must be between 0 and (size of list - 1) inclusive.

```
list[[INT]] = [VALUE];
```

***

### <a name="clear-list"></a> Empty out List

![empty list](https://static.stencyl.com/pedia2/block-images/attributes/lists/clear-list.png)

Removes all values from the list.

```
Utils.clear(list);
```

***

## Access

### <a name="get-item"></a> Get Item from Index

![get item # int from list](https://static.stencyl.com/pedia2/block-images/attributes/lists/get-item.png)

Returns the item at the specified index in the list. The index must be between 0 and (size of list - 1) inclusive.

```
list[[INT]]
```

***

### <a name="position-of-item"></a> Position of Item in List

![get position of object in list](https://static.stencyl.com/pedia2/block-images/attributes/lists/position-of-item.png)

Returns the index of the item in the list. If the item is in the list multiple times, this returns the first index found. If the item isn't in the list, this returns -1.

```
list.indexOf([VALUE])
```

***

### <a name="contains-item"></a> List contains Item?

![list contains object](https://static.stencyl.com/pedia2/block-images/attributes/lists/contains-item.png)

Returns `true` if the list contains the specified item.

```
Utils.contains(list, [VALUE])
```

***

### <a name="length-list"></a> List Size

![number of items in list](https://static.stencyl.com/pedia2/block-images/attributes/lists/length-list.png)

Returns the number of items in the list.

```
list.length
```

***

### <a name="is-empty"></a> Is List Empty?

![list contains no items](https://static.stencyl.com/pedia2/block-images/attributes/lists/is-empty.png)

Returns `true` if the list contains no items.

```
(list.length == 0)
```

***

### <a name="for-each"></a> For Each Item in List ...

![for each in list](https://static.stencyl.com/pedia2/block-images/attributes/lists/for-each.png)

Lets you perform logic on each item in the list. Use the embedded `item` block to retrieve the current item being examined.

```
for(item in cast(list, Array<Dynamic>)) {
  [ACTIONS]
}
```

***
