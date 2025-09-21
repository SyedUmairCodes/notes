# Introduction to Lists

A list is an ordered collection of items, lists can contain items of other data types and lists as well. Each item has an index value that is used to identify the item, the first item has the index value of 0 and so on.

In Python, square brackets `[]` indicate a list, and individual elements in the list are separated by commas.

```python
fruits = ["apple","banana", "mango","kiwi"]
print(fruits)
```

When you access the list directly it will print every single item that is in the list, this is due to not specifying an index value for the item we needed to retrieve.

```python
fruits = ["apple","banana", "mango","kiwi"]
print(fruits[2]) # mango will be printed
```

>[!NOTE]
>If the item stored in the list is a string, then all of the string methods can be applied to it when printing it on the console.

If you don't know the last item in the list and want to access it you can print it using negative indexes.

```python
fruits = ["apple","banana", "mango","kiwi"]
print(fruits[-1]) # kiwi will be printed
```

## Adding items

The items in a list can be modified easily, the syntax is similar to how we reassign values to variables, we just need to add the index of the item that we need to change.

```python
fruits = ["apple","banana", "mango","kiwi"]
fruits[3] = "orange"
print(fruits)
```

Lists are used to store values of similar type and can be used for visualization and many other purposes. The `append()` method allows you to add a new item to then end of the list.

```python
fruits = ["apple","banana", "mango","kiwi"]
fruits.append("peach")
print(fruits)
```

The `insert()` method is an alternative to the append method and allows you to add a new item to a list but you can specify which index you want to add the new item at.

## Removing items

Removing items from lists is similar to adding them, if you the know the index of the item just use the `del()` method to remove it and the `pop()` method is another way that you can use to remove the last item of a list or any other index if you know it.

>[!NOTE]
>If you’re unsure whether to use the `del()` statement or the `pop()` method, here’s a simple way to decide: when you want to delete an item from a list and not use that item in any way, use the `del()` statement; if you want to use an item as you remove it, use the `pop()` method.

When you don't know the index of the value but know the value itself then you can use the `remove()` method to remove that item from the list.

## Sorting items

The items in a list might not be sorted in an order that you want them to be. The `sort()` method will allow you to sort the items in your list in alphabetical or reverse-alphabetical order.

>[!IMPORTANT]
>The `sort()` method changes the list and the index values as well if you don't want that then use the `sorted()` method

## Reversing lists

To reverse the original order of a list, you can use the `reverse()` method. If you stored the list of cars in chronological order, we could easily rearrange the list into reverse-chronological order. `reverse()` doesn’t sort backward alphabetically; it simply reverses the order of the list.

> [!NOTE]
> The reverse() method changes the order of a list permanently, but you can revert to the original order anytime by applying reverse() to the same list a second time.

>[!TIP]
> The `len()` function allows you to list how many items are in a list.

## Index errors

The most common type of errors that you'll encounter when working with lists is the index error, this happens when you want to access an item but you put an index that doesn't exist or has the data type item.