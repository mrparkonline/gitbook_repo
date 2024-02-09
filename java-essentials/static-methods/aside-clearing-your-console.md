# (Aside) Clearing your Console

```java
public static void clearScreen() {  
    System.out.print("\033[H\033[2J");  
    System.out.flush();  
}
```

The static method called `clearScreen()` contains two output statements that should help to clear your console.

This is useful when you are making a console/text-only Java application and you need to reset the output being shown. Try implementing/copying the code over and calling the method.
