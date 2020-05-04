# READ1


## 1. C# Keywords:

|Category|	C# keywords|
|--------|-------------|
|Selection statements|	if, else, switch, case
Iteration statements|	do, for, foreach, in, while
Jump statements|	break, continue, default, goto, return, yield
Exception handling statements|	throw, try-catch, try-finally try-catch-finally|
|Checked and unchecked|	checked, unchecked|
|fixed statement|	fixed
|lock statement|	lock|

## 2. try Statements and Exceptions 
A try statement specifies a code block subject to error-handling or cleanup code. The try block must be followed by a catch block, a finally block, or both. The catch block executes when an error occurs in the try block. The finally block executes after execution leaves the try block (or if present, the catch block), to perform cleanup code, whether or not an error occurred. 

A try statement looks like this:<br>

try {  ... // exception may get thrown within execution of this block <br>
} 
catch (ExceptionA ex) { <br>
     ... // handle exception of type ExceptionA <br>
     } 
catch (ExceptionB ex) {<br>
      ... // handle exception of type ExceptionB<br>
       } 
finally { <br>
     ... // cleanup code <br>
     }


