# 📘 JavaScript

---

## Q1. What will be the output of the given code?

```js
<script>
var my_num = 15;
document.write(my_num.toString(16));
</script>
```

| # | Option | |
|---|--------|---|
| 1 | `f` | ✅ |
| 2 | `16` | |
| 3 | `Undefined` | |
| 4 | `NaN` | |

> ✅ **Answer: 1 — actual output is `f`**

> [!NOTE]
> `toString(16)` converts a number to its **hexadecimal** (base-16) string representation. 15 in hex is `f`. This is a trick question testing knowledge of `Number.prototype.toString(radix)`.

---

2. What would be the output of the following program ?

```java
import java.util.HashMap;
import java.util.Iterator;
import java.util.Set;

class Test {
    public static void main(String[] args) {
        HashMap t = new HashMap<>();
        t.put(null, 1);
        t.put(3, 2);
        Set s = t.keySet();
        Iterator iter = s.iterator();
        while(iter.hasNext()) {
            System.out.println(iter.next());
        }
    }
}
```

| # | Option | |
|---|--------|---|
| 1 | `3` | |
| 2 | `null 3` | ✅ |
| 3 | `Null Pointer Exception` | |
| 4 | `null` | |

> **Answer: 2 — Compilation fails / Runtime Error**

> [!NOTE]
> `Iterator iter = iterator();` is a **compile-time error** — `iterator()` is called without an object reference (should be `s.iterator()`). The code **will not compile**. If that typo were fixed, HashMap allows one `null` key, and iteration order is not guaranteed, but output would be `null` then `3`. The code as-is **fails at compilation**.

---

## Q3. Which of these classes implement the Collection interface SortedMap?

| # | Option | |
|---|--------|---|
| 1 | `HashMap` | |
| 2 | `HashTable` | |
| 3 | `TreeMap` | ✅ |
| 4 | `HashSet` | |

> ✅ **Answer: 3 — TreeMap**

> [!NOTE]
> `TreeMap` implements both `Map` and `SortedMap` interfaces. It stores keys in **sorted (natural) order**. `HashMap` and `HashTable` provide no ordering guarantee. `HashSet` implements `Set`, not `Map`. When you need sorted key traversal, `TreeMap` is the go-to.

---

## Q4. What is FALSE about `<meta>` tag?

| # | Option | |
|---|--------|---|
| 1 | Metadata will not display on page | |
| 2 | Tags always go inside the `<head>` element | ✅ |
| 3 | Metadata is data (information) about data | |
| 4 | The metadata can be used to identify, IIS verify | |

> ✅ **Answer: 2 — Tags always go inside the `<head>` element**

> [!NOTE]
> This is the FALSE statement. While `<meta>` tags are *conventionally* placed inside `<head>`, it is **not mandatory** — they can technically appear in `<body>` as well (though it's bad practice). The other statements are TRUE: metadata is invisible to users, it describes data about the document, and it can be used by servers and bots.

---

## Q5. If you do not put `<!DOCTYPE html>` in your `.html` file, will HTML5 work?

| # | Option | |
|---|--------|---|
| 1 | Yes, it will work because now `<html>` tag will enable all the features of HTML5 | |
| 2 | No, because the browser will not be able to identify that it is an HTML5 document, and HTML5 tags will not function properly | ✅ |
| 3 | Yes, because W3C has regulated `<html>` to mean HTML5 | |
| 4 | No, because `<!DOCTYPE html>` is the right format | |

> ✅ **Answer: 2**

> [!NOTE]
> Without `<!DOCTYPE html>`, the browser switches to **Quirks Mode** — it falls back to older, inconsistent rendering behavior. HTML5 features may still partially work, but layout and parsing won't follow the HTML5 spec reliably. Always declare `<!DOCTYPE html>` at the top of every HTML5 document.

---

## Q6. What will be the output of the following tag on an HTML5 web page?

```html
<center> Hi! This is new </center>
```

| # | Option | |
|---|--------|---|
| 1 | Center is not supported in HTML5 and is used in CSS instead | ✅ |
| 2 | Center will align the string to the center of the page | |
| 3 | Center will allow the user to decide on the location of text to be displayed | |
| 4 | The mentioned string moves from left to right | |

> ✅ **Answer: 1 — `<center>` is deprecated in HTML5**

> [!NOTE]
> The `<center>` tag was **deprecated in HTML4** and is **obsolete in HTML5**. Browsers may still render it for backward compatibility, but you should use CSS instead: `text-align: center` or `margin: auto`. Never use `<center>` in modern HTML.

---

## Q7. What will be the output of the following code snippet?

```java
public static void main(String args[]) {
    try {
        RandomAccessFile raf = new RandomAccessFile("myfile.txt", "r");
        byte b[] = new byte[1000];
        raf.readFully(b, 0, 1000);  
    } catch(IOException e) {
        System.err.println("File not found");
        System.err.println(e.getMessage());
        e.printStackTrace();
    } catch(FileNotFoundException e) {
        System.err.println("IO Error");
        System.err.println(e.toString());
        e.printStackTrace();
    }
}
```

| # | Option | |
|---|--------|---|
| 1 | Code compiles and executes without any error | |
| 2 | Runtime exceptions | |
| 3 | Compilation fails | ✅ |
| 4 | None of the above | |

> ✅ **Answer: 3 — Compilation fails**

> [!NOTE]
> `FileNotFoundException` is a **subclass** of `IOException`. In Java, you cannot catch a **more specific** exception (`FileNotFoundException`) **after** a **more general** one (`IOException`) — the compiler flags this as unreachable code. The rule: catch subclasses **before** superclasses. This is a classic Java exception ordering trap.

---

## Q8. What will be the outcome when the given code is compiled and run?

```java
class Test27 {
    public static void main(String args[]) {
        System.out.println(0.0 % 0.0 != 0.0 / 0.0);
    }
}
```

| # | Option | |
|---|--------|---|
| 1 | Compilation error | |
| 2 | `true` | ✅ |
| 3 | `false` | |
| 4 | `NaN` | |

> ✅ **Answer: 3 — `false`**

> [!NOTE]
> Both `0.0 % 0.0` and `0.0 / 0.0` evaluate to `NaN` in Java (IEEE 754 floating-point). The key rule: **`NaN != NaN` is always `true`** in Java. So the expression `NaN != NaN` evaluates to `true`... wait — but both sides are `NaN`, and `NaN != NaN` is `true``.

---

## Q9. What is the value returned by `parseInt("122", 2)`?

| # | Option | |
|---|--------|---|
| 1 | `1` | ✅ |
| 2 | `NaN` | |
| 3 | `Undefined` | |
| 4 | `0` | |

> ✅ **Answer: 1**

> [!NOTE]
> `parseInt("122", 2)` parses the string `"122"` in **base 2 (binary)**. Binary only uses digits `0` and `1`. It reads left to right: `1` is valid, `2` is **not a valid binary digit** — parsing stops there. So only `"1"` is parsed → result is **`1`**. If the string were `"101"`, the result would be 5.

---

## Q10. Wrapping of data members and member functions into a single entity (class) is called?

| # | Option | |
|---|--------|---|
| 1 | Inheritance | |
| 2 | Abstraction | |
| 3 | Encapsulation | ✅ |
| 4 | Polymorphism | |

> ✅ **Answer: 3 — Encapsulation**

> [!NOTE]
> **Encapsulation** is the OOP principle of bundling data (fields) and the methods that operate on them into a single unit (a class), and restricting direct access to the internals via access modifiers (`private`, `protected`). Think of it as a capsule that hides the implementation. It's the foundation of data hiding and clean APIs.

---

## Q11. What would be the output of the below code?

```java
class Multi extends Thread {
    public void run() {
        System.out.println("running");
    }
    public static void main(String args[]) {
        Multi t1 = new Multi();
        t1.start();
        t1.start();
    }
}
```

| # | Option | |
|---|--------|---|
| 1 | It will print `running` 2 times | |
| 2 | It will print `running` 1 time & then exit | |
| 3 | It will print `running` 1 time & then throw `IllegalThreadStateException` | ✅ |
| 4 | It will not print anything and only throw `IllegalThreadStateException` | |

> ✅ **Answer: 3**

> [!NOTE]
> A Java `Thread` can only be started **once**. The first `t1.start()` launches the thread and prints `"running"`. The second `t1.start()` on an already-started thread throws **`IllegalThreadStateException`** at runtime. This is a classic Java threading trap — always create a new `Thread` instance if you need to run it again.

---

## Q12. What would be the output of the following Java code?

```java
class q33 {
    public static void main(String args[]) {
        float f[] = new float[5];
        Object obj = f;
        System.out.println(f[0]);
    }
}
```

| # | Option | |
|---|--------|---|
| 1 | Compilation Error | |
| 2 | Runtime Exception | |
| 3 | `0.0` | ✅ |
| 4 | `0` | |

> ✅ **Answer: 3 — `0.0`**

> [!NOTE]
> In Java, arrays are objects. A `float[]` can be assigned to `Object` (upcasting — perfectly valid). Float array elements are **default initialized to `0.0f`**. `System.out.println(f[0])` prints the first element → **`0.0`**. The `Object obj = f` line is a red herring — it doesn't affect `f` at all.

---

## Q13. What will be the output of the given code?

```js
var my_arr = [3, 6, 2, 8];
function myFunction(elem) {
    return (elem < 10);
}
document.write(my_arr.every(myFunction));
```

| # | Option | |
|---|--------|---|
| 1 | `8` | |
| 2 | `true` | ✅ |
| 3 | `false` | |
| 4 | error | |

> ✅ **Answer: 2 — `true`**

> [!NOTE]
> `Array.prototype.every()` returns `true` if **all elements** satisfy the callback. Here every element `[3, 6, 2, 8]` is less than `10` → `every()` returns `true`. Note: the code has a typo `myFunciton` vs `myFunction` — if that typo existed in the actual test, it would throw a `ReferenceError`. Assuming it's correct, the answer is `true`.

---

## Q14. What does the following function indicate?

```js
function createSource(buffer) {
    var source = context.createBufferSource();
    var gainNode = context.createGain();
    source.buffer = buffer;
    source.loop = true;
    source.connect(gainNode);
    gainNode.connect(context.destination);
    return {
        source: source,
        gainNode: gainNode
    };
}
```

| # | Option | |
|---|--------|---|
| 1 | Low-pass filter | |
| 2 | Cross fading | ✅ |
| 3 | Playlist cross fading | |
| 4 | None of the given options | |

> ✅ **Answer: 2 — Cross fading**

> [!NOTE]
> This is a **Web Audio API** function. `createBufferSource()` creates an audio source, and `createGain()` creates a volume control node. The pattern of connecting a source → gainNode → destination is the standard setup for **cross-fading** between audio tracks — you fade one track's gain down while fading another's up. `source.loop = true` keeps it looping, which is typical for seamless cross-fade implementations.

---

## Q15. Which of the following strategies can design a browser with advanced features for better web pages?

| # | Option | |
|---|--------|---|
| 1 | Web 2.0 | |
| 2 | Progressive Enhancement | ✅ |
| 3 | Design Forward | |
| 4 | Graceful Degradation | |

> ✅ **Answer: 2 — Progressive Enhancement**

> [!NOTE]
> **Progressive Enhancement** is a web design strategy that starts with a baseline of core content/functionality that works everywhere, then layers advanced features on top for capable browsers. It ensures all users get a usable experience, with modern browsers getting richer ones. The opposite strategy is **Graceful Degradation** (build for modern first, then handle older browsers). "Design Forward" is not a standard term.

---

## Q16. Which of the following can be used to copy an array?

| # | Option | |
|---|--------|---|
| 1 | `.splice()` | |
| 2 | `.slice()` | ✅ |
| 3 | `.copy()` | |
| 4 | None | |

> ✅ **Answer: 2 — `.slice()`**

> [!NOTE]
> `array.slice()` (called with no arguments) returns a **shallow copy** of the entire array. `.splice()` **mutates** the original array by removing/replacing elements. `.copy()` does not exist in JavaScript. For a deep copy, use `JSON.parse(JSON.stringify(arr))` or `structuredClone(arr)`.

---

## Q17. We can run tests outside of Eclipse by using —

| # | Option | |
|---|--------|---|
| 1 | `org.junit.runner.JUnitCore` class | ✅ |
| 2 | `@org.junit.Test` | |
| 3 | Run → Run As → JUnit Test | |
| 4 | `@Suite.SuiteClasses` | |

> ✅ **Answer: 1 — `org.junit.runner.JUnitCore`**

> [!NOTE]
> `JUnitCore` is JUnit's facade for running tests programmatically from the **command line or any Java program**, outside of an IDE like Eclipse. You call `JUnitCore.runClasses(YourTest.class)`. Options 2 and 4 are annotations, not runners. Option 3 is Eclipse-specific IDE functionality.

---

## Q18. Which of the following codes is used to read the last 10 bytes of a file which is 100 bytes long?

| # | Option | |
|---|--------|---|
| 1 | `fs.createReadStream('sample.txt', { start: 90, end: 99 })` | ✅ |
| 2 | `fs.readFile('sample.txt', { start: 10, end: 100 })` | |
| 3 | `file.read('sample.txt', { start: 90, end: 99 })` | |
| 4 | `file.stream('sample.txt', { start: 10, end: 100 })` | |

> ✅ **Answer: 1**

> [!NOTE]
> This is a **Node.js** question. `fs.createReadStream()` accepts `start` and `end` byte offsets (both inclusive). For a 100-byte file, bytes are indexed 0–99. The last 10 bytes → `start: 90, end: 99`. `fs.readFile()` does not support `start`/`end` options. `file.read` and `file.stream` are not valid Node.js `fs` module APIs.

---

## Q19. What will be the output on the console for the following AngularJS code?

```html
<!-- shop.html -->
<!doctype html>
<html ng-app="bagApp">
  <head>
    <title>Angular SPA</title>
    <script src="lib/Angular/angular.js"></script>
    <script src="js/app_customdirective.js"></script>
  </head>
  <body>
    <center>
      <headerline title="'Shop Your Bags Online'"></headerline>
    </center>
  </body>
</html>
```

| # | Option | |
|---|--------|---|
| 1 | `(controller) (compile) (pre-link) (post-link)` | |
| 2 | `(pre-link) (compile) (controller) (post-link)` | |
| 3 | `(compile) (pre-link) (controller) (post-link)` | |
| 4 | `(compile) (controller) (pre-link) (post-link)` | ✅ |

> ✅ **Answer: 4 — `(compile) (controller) (pre-link) (post-link)`**

> [!NOTE]
> This tests the **AngularJS custom directive lifecycle**. The correct order of execution for a directive is:
> 1. **compile** — DOM transformation before instances are created
> 2. **controller** — sets up scope and controller logic
> 3. **pre-link** — runs before child directives are linked
> 4. **post-link** — runs after all children are linked (most logic goes here)
>
> This is an important Angular 1.x interview topic.

---

## Q20. Which jQuery function adds HTML content **outside** a selection?

| # | Option | |
|---|--------|---|
| 1 | `outside()` | |
| 2 | `after()` | ✅ |
| 3 | `later()` | |
| 4 | `more()` | |

> ✅ **Answer: 2 — `after()`**

> [!NOTE]
> `$(selector).after(content)` inserts content **immediately after** (outside of) the selected element in the DOM. Its sibling `before()` inserts before it. For inserting inside an element, use `append()` (at end) or `prepend()` (at beginning). `outside()`, `later()`, and `more()` are not jQuery methods.

---

## Q21. Which of the following statements is NOT true about JavaScript function names?

| # | Option | |
|---|--------|---|
| 1 | They can include underscore | |
| 2 | They can start with a letter | |
| 3 | They are not case sensitive | ✅ |
| 4 | None of the above | |

> ✅ **Answer: 3 — They are not case sensitive**

> [!NOTE]
> This statement is **FALSE** — JavaScript function names **are case-sensitive**. `myFunction` and `MyFunction` are two completely different identifiers. Valid JS identifiers can start with a letter, `_`, or `$`, and can contain underscores — so options 1 and 2 are both true. Case-sensitivity applies to all JS identifiers.

---

## Q22. Why is `stop()` method added before calling `animate()`?

| # | Option | |
|---|--------|---|
| 1 | `stop()` halts execution of all scripts until animation finishes | |
| 2 | `stop()` ends any currently running animation on the element & prevents conflicts & pile-ups | ✅ |
| 3 | The user tells jQuery that the animation has to be stopped at some point | |
| 4 | None of the above | |

> ✅ **Answer: 2**

> [!NOTE]
> When a jQuery animation is triggered repeatedly (e.g. on `hover`), animations **queue up** and play one after another — causing a "pile-up" effect. Calling `.stop()` before `.animate()` **clears the current animation queue**, ensuring the new animation starts cleanly without waiting for previous ones. This is especially important for hover effects.

---

## Q23. Which of the following is used to hide information in Object Oriented Programming?

```
a. Encapsulation
b. Inheritance
c. Abstraction
d. Polymorphism
```

| # | Option | |
|---|--------|---|
| 1 | `a, c` | ✅ |
| 2 | `a, b` | |
| 3 | `b, c` | |
| 4 | `a, d` | |

> ✅ **Answer: 1 — a & c (Encapsulation and Abstraction)**

> [!NOTE]
> Both **Encapsulation** and **Abstraction** are used for information hiding:
> - **Encapsulation** hides the *internal state* (data) using access modifiers like `private`
> - **Abstraction** hides the *implementation details*, exposing only the interface (what it does, not how)
>
> **Inheritance** is about reusing code from a parent class. **Polymorphism** is about one interface having multiple behaviors. Neither directly hides information.

---

## Q24. Which one of the following is equivalent to Line 1?

```java
interface ITest {
    void show(); // Line 1
}
```

| # | Option | |
|---|--------|---|
| 1 | `public final void show()` | |
| 2 | `public abstract void show()` | ✅ |
| 3 | `public abstract final void show()` | |
| 4 | `public static void show()` | |

> ✅ **Answer: 2 — `public abstract void show()`**

> [!NOTE]
> In Java, all methods declared in an interface are **implicitly `public` and `abstract`** (before Java 8 default/static methods). So `void show()` is equivalent to `public abstract void show()`. It cannot be `final` (because `abstract` and `final` contradict each other — `final` means no override, `abstract` demands it). It cannot be `static` either, as that would not require implementation.

---

## Q25. In the class below, is method `getIt()` thread-safe?

```java
public class X {
    private byte myVar;
    public void setIt(byte var) {
        myVar = var;
    }
    public long getIt() {
        return myVar;
    }
}
```

| # | Option | |
|---|--------|---|
| 1 | Yes | ✅ |
| 2 | No | |

> ✅ **Answer: 1 — Yes**

> [!NOTE]
> `myVar` is a `byte` — reads and writes to `byte` variables are **atomic** in Java (per the JVM spec, 32-bit and smaller primitive reads/writes are atomic). `getIt()` simply reads and returns `myVar`, which is an atomic read. So `getIt()` is **thread-safe in isolation**. However, the class as a whole is *not* thread-safe — a `setIt()` followed by `getIt()` by another thread has no memory visibility guarantee without `volatile` or `synchronized`. The question asks only about `getIt()`.

---

## Q26. What will be the output of the following code?

```java
class DemoCode {
    public static void main(String args[]) {
        byte b = 1;
        b += 1;
        System.out.println(b);
    }
}
```

| # | Option | |
|---|--------|---|
| 1 | `2` | ✅ |
| 2 | Compilation Error | |
| 3 | `1` | |
| 4 | Runtime Exception | |

> ✅ **Answer: 1 — `2`**

> [!NOTE]
> `b += 1` is a **compound assignment operator** in Java, which includes an **implicit cast**. It is equivalent to `b = (byte)(b + 1)`. Without the compound form, `b = b + 1` would fail to compile because `b + 1` promotes to `int`. Since `b` starts as `1` and we add `1`, the result is `2`. This is a classic Java type promotion gotcha — always use `+=` when incrementing `byte` or `short` variables.

---
