Javascript MyC

---

1. What will be the output of the given code ?

```js
<script>
var my_num = 15;
document.write(my_num.toString(16));
</script>
```

options:
1. 1
2. 0
3. Undefined
4. NaN

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
        t.put(3,2);
        Set s = t.keySet();
        Iterator iter = iterator();
        while(iter.hasNext()) {
            System.out.println(iter.next());
        }
    }
}
```

options:
1. 3
2. null 3
3. Null Pointer Exception
4. null


---

3. Which of these classes implement the Collection interface SortedMap ?

options:
1. HashMap
2. HashTable
3. TreeMap
4. HashSet


---

4. What is FLASE about tage

options:
1. metadata will not display on page
2. tags always go inside the elemnt
3. metadata is data(information) about data
4. The metadata can be used to identify IIS verify

---

5. If you do not put <!DOCTYPE html> in your .html file, will HTML5 work ?

options:
1. Yes it will work because now <html> tag willl enable all the features of HTML5
2. No, because the browswer will ont be able to identify that it is an HTML5 document, and HTML5 taqgs will not function properly
3. Yes, because W3C has regulates for <html> means HTML5 tags
4. No, because <! DOCTYPE html> is the rright format

---


6. What will be the output of the following tag on a HTML5 web page ?
```js
<center> Hi! This is new </center>
```

options:
1. Center is not supported in HTML5 and is used in CSS instead
2. Center will align the string to the center of the page
3. Center will allow the user to decide on the location of text to displayed
4. The mentioned string move from left to right

---

7. what will be the output of the following code snippet ? 

```java
public static void main(String args[]) {
    try {
        RandomAccessFile raf = new RandomAccessFile("myfile.txt", "r");
        byte b[] = new byte[1000];
        raf.readFully(bm 0, 1000);
    } catch(IOException e) {
        System.err.println("File not fonud");
        System.err.println(e.getMessage());
        e.printStackTrace();
    } catch(FileNotFoundException e) {
        System.err.println("IO Error");
        System.err.println(e.toString());
        e.printStackTrace();
    }
}
```

options:
1. Code compiles and executes without any error
2. Runtime exceptions
3. compilation fails
4. none of the above

---

8. What will be the outcome when the given ocde is compiled and run?

```java
class Test27 {
    public static void main(String args[]) {
        System.out.println(0.0%0.0!=0.0/0.0);
    }
}
```

options:
1. compilation error
2. true
3. false
4. NaN

---

9. What is the value returned by the JavaScript statemetn, parseInt("122", 2); ?

options:
1. 1
2. NaN
3. Undefined
4. 0

---

10. Wrapping of data memeber and member funciton into single entity class is called ?

options:
1. Inheritance
2. Abstraction
3. Encapsulation
4. Polymorphism

---

11.  What would be output of below code /

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

options:
1. It will print running 2 time
2. It will print running 1 time & then exit
3. It will print running 1 time & then throw Illegal Thread State Exception
4. It willnot print anything and only throw illegal Thread State Exceptino

---

12. What would be the output of the foolwoing Java code ?

```java
class q33 {
    public static void main(String args[]) {
        float f[] = new float[5];
        Object obj = f;
        System.out.println(f[0]);
    }
}
```

options:
1. Compilation Error
2. Runtime Exception
3. 0.0
4. 0

---

13. What will be the output of the given code ?

```js
var my_arr = [3,6,2,8];
function myFunction(elem) {
    return (elem < 10);
}
document.write(my_arr.every(myFunciton));
```

options:
1. 8
2. true
3. false
4. error

---

14.  What does the following funciotn indicate ?

```js
function createSource(buffer) {
    var source = context.createBufferSource();
    var gainNode = context.crateGain();
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

options:
1. Low-pay filter
2. cross fading
3. Playlight cross fading
4. None of the given option

---

15. Which of the following strategies can design a browswer with advanced features better web pages ?

options:
1. Web 2.0
2. Progressive Enhancement
3. Design Forward
4. Delicate Degradation

---

16. Which of the following can be used to copy an array?

options:
1. .splice
2. .slice
3. .copy
4. none

---

17. We can run test outside of Eclispse by using - 

options:
1. org.junit.runner.JUnitCore class
2. @org.junit.Test
3. Run -> Run As -> JUnitTest
4. @Suitee.SuiteClasses

---

18. Which of the following codes is used to read the last 10 bytes of a file which is 100 bytes long ?

options:
1. fs.createReadStream('sample.txt', { start: 90, end: 99});
2. fs.readFile('sample.txt', {start: 10, end: 100});
3. file.read('sample.txt', {start: 90, end: 99});
4. file.stream('sample.txt', {start: 10, end: 100});

---

19. What will be the output of the following code snippet on console ? 

```js
========shop.html=======
<!doctype html> 
<html ng-app = "bagApp">
    <head>
        <title>Angular SPA</title>
    <!-- In the below script tag srchas the pat of Angular library which is locally in the app -->
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

options:
1. (controller) (compile) (pre-link) (post-link)
2. (pre-link) (compile) (controller) (post-link)
3. (compile) (pre-link) (controller) (post-link)
4. (compile) (controller) (pre-link) (post-link)

---

20. Which jQuery function adds HTML content outside a selection ?

options:
1. outside()
2. after()
3. later()
4. more()

---

21. Which of the following statements is not true about JavaScript funcitno ?

options:
1. They can include underscore
2. They can start with letter
3. They are not case sensitive
4. None of the above

---

22. Why is stop() method added before calling animate() ?

options:
1. stop() halts the execution of the scripts on the page until the animation has finished
2. stop() ends any currently running animation on the element & prevents conflicts & pile ups
3. the user tell jquery that the animation has to be stopped at some point
4. none of the above

---

23. Which of the following is used to hide information in Object oriented programming 

a. Encapsulation 
b. Inheritance 
c. ABstraction
d. Polymorphism

options:
1. ac
2. ab
3. bc
4. ad

---

24. Which one of the following is equivalent to kine 1 

```java
interface ITest {
    void shot(); // Line 1
}
```

options:
1. public final void show()
2. public abstract void show()
3. public abstract final void show()
4. public static void show()

---

25. In the calss below, is method getIt() thread safe ?

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

options:
1. Yes
2. No

---

26. What will be the output of the following code ?

```java
class DemoCode {
    public static void main (Stirng args[]) {
        byte b = 1;
        b+ =1;
        System.out.println(b);
    }
}
```

options:
1.  
2. 
3. 
4. 

---

