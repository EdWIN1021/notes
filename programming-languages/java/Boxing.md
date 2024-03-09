## Boxing

Boxing is the process of converting a primitive type to its corresponding wrapper class.

 
```java
Integer boxedInt = Integer.valueOf(15);
Integer boxedInt = new Integer(15);
```

---

## Auto-boxing

```java
Integer boxedInt = 15;
```

---

## Unboxing

Unboxing is the process of extracting the primitive value from a wrapper class.

```java
Integer boxedInteger = 15;
int unboxedInt = boxedInteger.intValue();
```


```js


const a = "eee";

var levelOrder = function (root) {
  if (!root) return [];

  const res = [];
  const q = [root];

  while (q.length) {
    let length = q.length;
    let temp = [];

    for (let i = 0; i < length; i++) {
      const node = q.shift();
      temp.push(node.val);
      if (node.left) {
        q.push(node.left);
      }
      if (node.right) {
        q.push(node.right);
      }
    }
    res.push(temp);
  }

  return res;
};
```