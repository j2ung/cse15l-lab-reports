## Lab 3 - Bugs and Commands

# Bugs
1. Failure Inducing Input With `reverseInPlace` 
```
@Test 
  public void testReverseInPlace2() {
    int[] customInput2 = {1, 2, 3};
    ArrayExamples.reverseInPlace(customInput2);
    assertArrayEquals(new int[]{3, 2, 1}, customInput2);
    }
```
  
2. Failure Not From Inducing Input With `reverseInPlace`
```
@Test
public void testReverseInPlace3() {
    int[] customInput3 = {1};
    ArrayExamples.reverseInPlace(customInput3);
    assertArrayEquals(new int[]{1}, customInput3);
}
```
3. The Symptom
  ![Image](lab3-ss1.png)

4. The Bug Before And After Code Change

Before:
```
static void reverseInPlace(int[] arr) {
    for (int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

After:
```
  static void reverseInPlace(int[] arr) {
    int[] temp = new int[arr.length];
    for (int i = 0; i < arr.length; i++){
      temp[i] = arr[i];
    }
    for (int i = 0; i < arr.length; i += 1) {
      arr[i] = temp[arr.length - 1 - i];
    }
  }
```


# Researching Commands 
(used ChatGTP) 
1. grep using `-v`
```
grep -v "pig" results.txt
  cow
  chicken
  chicken
  dog
  chicken
  cat
```
or

```
grep -rv "cow" /Users/juliaung/docsearch/results.txt
  pig
  chicken
  pig
  chicken
  dog
  chicken
  cat
  pig
```
* `-v` will invert the search and will exclude the input. This is important because it will easy remove unnessary elements and print the rest of the content.
2. grep using `-c`
```
grep -c "pig" results.txt
3
```
or 

```
grep -c "No Words" /Users/juliaung/docsearch/results.txt
0
```
* `-c` will count the lines that contain the input. This is useful because it will count and return the reoccurance of the element.

3. grep using `-1`
```
grep -1 "pig" results.txt
  pig
  pig
  pig
```
or 

```
grep -1 "No Words" /Users/juliaung/docsearch/results.txt
  pig
  pig
  pig
```
* `-1` is the opposite of `-v` where it will print the input. This is convenient because it will reduce the content to a managable amount. It remove all that does not include the input.
