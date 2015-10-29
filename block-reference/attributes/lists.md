# Attributes > Lists

***

> Read our article on [Lists](http://www.stencyl.com/help/view/lists/) for an explanation of these blocks.

***

## Add / Insert

### Add Item to List

![add-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/add-list.png)

aaa

```
list.push([VALUE]);
```

***

### Insert Item into List

![insert-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/insert-list.png)

aaa

```
list.insert([NUMBER], [VALUE]);
```

***

## Remove

### Remove Item from List

![remove-item-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/remove-item.png)

aaa

```
list.remove([VALUE]);
```

***

### Remove Item from Index

![remove-index-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/remove-index.png)

aaa

```
list.splice([NUMBER], 1);
```

***

### Empty List

![empty-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/clear-list.png)

aaa

```
Utils.clear(list);
```

***

## Replace

### Replace Item in List

![replace-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/replace-list.png)

aaa

```
list[[NUMBER]] = [VALUE];
```

***

## Getters

### Get Item from Index

![get-index-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/get-item.png)

aaa

```
list[[NUMBER]]
```

***

### List contains Item?

![contains-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/contains-item.png)

aaa

```
Utils.contains(list, [VALUE])
```

***

### List Size

![size-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/length-list.png)

aaa

```
list.length
```

***

### Is List Empty?

![is-empty-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/is-empty.png)

aaa

```
(list.length == 0)
```

***

## Create / Copy

### Create New List

![create-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/create-list.png)

aaa

```
new Array<Dynamic>()
```

***

### Copy of List

![copy-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/copy-list.png)

aaa

```
list.copy()
```

***

## Looping

### Add Item to List

![loop-list-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/3%20-%20Lists/for-each.png)

aaa

```
for(item in cast(list, Array<Dynamic>)) {
	
}
```

***
