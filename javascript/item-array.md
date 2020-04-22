# ลบ item ใน array

{% embed url="https://flaviocopes.com/how-to-remove-item-from-array/" %}

## ถ้ารู้ Index

```javascript
const items = ['a', 'b', 'c', 'd', 'e', 'f']
const i = 2
const filteredItems = items.slice(0, i).concat(items.slice(i + 1, items.length))
// ["a", "b", "d", "e", "f"]
```

## ถ้ารู้ค่า

```javascript
const items = ['a', 'b', 'c', 'd', 'e', 'f']
const valueToRemove = 'c'
const filteredItems = items.filter(item => item !== valueToRemove)
// ["a", "b", "d", "e", "f"]
```

```javascript
const items = ['a', 'b', 'c', 'd', 'e', 'f']
const valueToRemove = 'c'
const filteredItems = items.filter(function(item) {
  return item !== valueToRemove
})
// ["a", "b", "d", "e", "f"]
```

## ลบหลาย item

### ลบด้วย index

```javascript
const items = ['a', 'b', 'c', 'd', 'e', 'f']

const removeItem = (items, i) =>
  items.slice(0, i-1).concat(items.slice(i, items.length))

let filteredItems = removeItem(items, 3)
filteredItems = removeItem(filteredItems, 5)
//["a", "b", "d", "e"]
```

### ลบด้วยค่า

```javascript
const items = ['a', 'b', 'c', 'd', 'e', 'f']
const valuesToRemove = ['c', 'd']
const filteredItems = items.filter(item => !valuesToRemove.includes(item))
// ["a", "b", "e", "f"]
```



splice\(\) เพื่อไม่ให้สับสนกับ slice\(\) มันจะกลับไป array แรกเริ่ม พยายามอย่าใช้มัน





