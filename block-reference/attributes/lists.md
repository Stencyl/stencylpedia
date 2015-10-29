# Attributes > Lists

***

> Read our article on [Lists](http://www.stencyl.com/help/view/lists/) for an explanation of these blocks.

***

## Add / Insert

### Add Item to List

![add-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/add-list.png)

Adds the given value to the end of the list.

```
list.push([VALUE]);
```

***

### Insert Item into List

![insert-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/insert-list.png)

Inserts the given value at the specified index of the list. This will push everything at that index and after down one position. The index must be between 0 and (size of list - 1) inclusive.

```
list.insert([NUMBER], [VALUE]);
```

***

## Remove

### Remove Item from List

![remove-item-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/remove-item.png)

Removes the given value from the list, if it exists. If it does not exist, nothing happens.

```
list.remove([VALUE]);
```

***

### Remove Item from Index

![remove-index-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/remove-index.png)

Removes the value at the specified index from the list. The index must be between 0 and (size of list - 1) inclusive.

```
list.splice([NUMBER], 1);
```

***

### Empty out List

![empty-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/clear-list.png)

Removes all values from the list.

```
Utils.clear(list);
```

***

## Replace

### Replace Item in List

![replace-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/replace-list.png)

Replaces the item at the specified index with another for the list. The index must be between 0 and (size of list - 1) inclusive.

```
list[[NUMBER]] = [VALUE];
```

***

## Getters

### Get Item from Index

![get-index-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/get-item.png)

Returns the item at the specified index in the list. The index must be between 0 and (size of list - 1) inclusive.

```
list[[NUMBER]]
```

***

### List contains Item?

![contains-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/contains-item.png)

Returns `true` if the list contains the specified item.

```
Utils.contains(list, [VALUE])
```

***

### List Size

![size-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/length-list.png)

Returns the number of items in the list.

```
list.length
```

***

### Is List Empty?

![is-empty-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/is-empty.png)

Returns `true` if the list contains no items.

```
(list.length == 0)
```

***

## Create / Copy

### Create New List

![create-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/create-list.png)

Creates and returns an empty list. Usually, you'll want to set this immediately to a list attribute.

```
new Array<Dynamic>()
```

***

### Copy of List

![copy-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/copy-list.png)

Returns a shallow copy of the specified list.

```
list.copy()
```

***

## Looping

### For Each Item in List

![loop-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/for-each.png)

Lets you perform logic on each item in the list. Use the embedded `item` block to retrieve the current item being examined.

```
for(item in cast(list, Array<Dynamic>)) {
  [ACTIONS]
}
```

***
