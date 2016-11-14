[![05AB1E][1]][1]


A new (experimental) golfing language. If the name **05AB1E** was interpreted as a hexadecimal number and converted to base64, it would result into "Base". I wanted to make a language which has an advantage in base conversion, but now it is more of an overall language.

You can try this language out yourself at: [Try it online!](http://05ab1e.tryitonline.net/). This interpreter is provided by [DennisMitchell](https://github.com/DennisMitchell).

All existing commands can be found at [_Info.txt_](https://github.com/Adriandmen/05AB1E/blob/master/Info.txt)


### So, what exactly is a golfing language?

A golfing language is a language that specializes in [code golf](https://en.wikipedia.org/wiki/Code_golf). That is a kind of programming competition where you strive to achieve the shortest byte count from all the participating languages.

### What does a program look like?

#### The basics

A program in 05AB1E is just like any other program, it is stored in a file and then run with **05AB1E.py**. The python file will interpret the given file as 05AB1E code. A very easy to understand program is:

    "Hello, World!"

Which can be tried [here](http://05ab1e.tryitonline.net/#code=IkhlbGxvLCBXb3JsZCEi&input=). This is a normal `Hello, World!` program. Of course, the last quotation mark is a bit redundant, so we can actually leave that out. The interpreter will **automatically** complete the string. That means that the following program:

    "Hello, World!

is also a valid `Hello, World!` program.

#### Stack memory

05AB1E uses a stack memory model. That means that everything will be operated using the stack. For example, if we want to multiply 2 different numbers, let's say **4** and **5**, we can do the following in pseudo-stack language:

    PUSH 4
    PUSH 5
    MULTIPLY

After the first **two** commands, the top two elements of the stack are `4` and `5`. The multiply command _consumes_ two elements and produces one in return. So, after the multiply command, the stack only contains the number `20`. So, how do we do this in 05AB1E?

To push an integer, just place any arbitrary integer in the progam. For example, if we want to push the number **4**, this would be our program:

    4

05AB1E will scan the literal up till no more digits are found and pushes that onto the stack. To push a new number, just add another number after the first number, separated by a no-op (like a space). For example:

    4 15

This pushes the numbers **4** and **15**.

#### Integers and strings

One of the things that makes 05AB1E special is that a string and an integer are the same type. That means that you can both perform string operations on ints, as well as int operations on strings (if possible). That said, let's see how you _can_ perform integer operations.



  [1]: https://i.stack.imgur.com/kUDMr.png
