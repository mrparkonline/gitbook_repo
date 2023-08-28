# IPO Model

An _**Input-Processing-Output (IPO) Model**_ is a tool that helps to design basic programs. By using an IPO Model, it eases the process of translating our requirements to code.

### Our Example Problem

> The client has requested for a Fahrenheit to Celsius converting program

#### Input Analysis

> **Input:** Analyzing the inputs that the program requires to solve the given problem

* The program needs to be given a Fahrenheit value.
* It should be a numeric value that supports decimals and negatives

#### Processing Analysis

> **Processing:** Analyzing how we would use the input to calculate or process our inputs and variables

```
    let F represent fahrenheit
    let C represent celsius
    
    (F − 32) × 5/9 = C
```

* To convert a Fahrenheit temperature to Celsius, we can use the the formula stated above

#### Output Analysis

> **Output:** Stating the expected output after processing is done

* The program can output the conversion as a text
