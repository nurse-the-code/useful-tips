## Table of Contents
- General
  - [Run a program](#run-a-program)
- Commandline IO
  - [Print to terminal](#print-to-terminal)
  - [Capture user input](#capture-user-input)
- File IO
  - [Read a file](#read-a-file)

## General
### Run a program
```
public class Foo {

    public static void main(String[] args) {
    
    // Code starts running in this code block
    }
}
```

## Commandline IO
### Print to terminal
- To print output with a line return: `System.out.println("Text to print goes here.");`
- To print output without a line return: `System.out.println("Text to print goes here.");`
- To print formated text (line return not included): `System.out.format("Text to print go here and %s", "other arguments go here");`

### Capture user input
```
Scanner input = new Scanner(System.in); // create Scanner object to capture keyboard stream
System.out.print("Type something in: ");  // prompt user for input
String userInput = input.nextLine();  // accept keyboard input from user until they hit enter; save input as a String variable
```

### Colored text and colored background in text
To print a single line of green text
```
public class foo {

    public static final String ANSI_RESET = "\u001B[0m";
    public static final String ANSI_GREEN = "\u001B[32m";

    public static void main(String[] args) {
    
        `System.out.println(ANSI_GREEN + "This text is green!" + ANSI_REST + " But this text is not green.");`
    }
}
```

To text with a blue background:
```
public class foo {

    public static final String ANSI_RESET = "\u001B[0m";
    public static final String ANSI_BLUE_BACKGROUND = "\u001B[44m";

    public static void main(String[] args) {
    
        `System.out.println(ANSI_BLUE_BACKGROUND + "This background is blue!" + ANSI_REST + " But this background is not blue.");`
    }
}
```

Basic color library:
```
// For reseting color
public static final String ANSI_RESET = "\u001B[0m";
 
// For changing color of text
public static final String ANSI_BLACK = "\u001B[30m";
public static final String ANSI_RED = "\u001B[31m";
public static final String ANSI_GREEN = "\u001B[32m";
public static final String ANSI_YELLOW = "\u001B[33m";
public static final String ANSI_BLUE = "\u001B[34m";
public static final String ANSI_PURPLE = "\u001B[35m";
public static final String ANSI_CYAN = "\u001B[36m";
public static final String ANSI_WHITE = "\u001B[37m"; 

// For changing color of text background
public static final String ANSI_BLACK_BACKGROUND = "\u001B[40m";
public static final String ANSI_RED_BACKGROUND = "\u001B[41m";
public static final String ANSI_GREEN_BACKGROUND = "\u001B[42m";
public static final String ANSI_YELLOW_BACKGROUND = "\u001B[43m";
public static final String ANSI_BLUE_BACKGROUND = "\u001B[44m";
public static final String ANSI_PURPLE_BACKGROUND = "\u001B[45m";
public static final String ANSI_CYAN_BACKGROUND = "\u001B[46m";
public static final String ANSI_WHITE_BACKGROUND = "\u001B[47m";
```

For further details see [Wikipedia](https://en.wikipedia.org/wiki/ANSI_escape_code#Colors)
and [StackOverflow](https://stackoverflow.com/questions/5762491/how-to-print-color-in-console-using-system-out-println).
