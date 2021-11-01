## isEmpty系列

#### StringUtils.isEmpty()

是否为空，可以看到“ ”空格是会绕过这种判断，因为是一个空格，并不是严格的空值，会导致isEmpty(" ") = false

```java
	StringUtils.isEmpty(null) = true
  StringUtils.isEmpty("") = true
  StringUtils.isEmpty(" ") = false
  StringUtils.isEmpty("test") = false
  StringUtils.isEmpty(" test ") = false
```

