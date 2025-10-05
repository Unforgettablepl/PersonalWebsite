---
title: "GDB – The GNU Debugger"
description: "A cheatsheet for the GNU Debugger"
date: 2025-10-05
---
### Author: Samik Goyal
---
The best way to debug C++ programs.

---
## Before we start

1) Always compile your programs with `-g`. This adds debugging information that GDB uses.
2) Never use `-O2`,`-O3`, or `-Ofast` when using GDB. It will make it hard to debug.
3) It might ask you `Enable debuginfod for this session?`. Just use `n` or press enter directly (`n` is default).
4) Use the std library's debug mode (`-DGLIBCXX_DEBUG`).

---
## TUI (Text User Interface) Mode

### **Start GDB with TUI**

`gdb --tui <program>`\
Opens GDB in a split-screen interface showing source code alongside the command prompt.

### **Quiting**

`q`\
:)

---

## Run and Control Execution

### **Run**

`r [arguments]`\
Runs the program with optional command-line arguments.

### **Next**

`n`\
Runs the current line and then pauses again on the next line.

### **Continue**

`c`\
Continues program execution until the next breakpoint or program end.

### **Finish**

`finish`\
Executes until the current function returns, then stops. Will also display the returned value. Useful when you **just need to know** the return value.

---

## Breakpoints and Conditions

GDB will automatically pause execution if a runtime error occurs. Otherwise, it will only pause execution when a breakpoint is reached.

### **Set Breakpoint**

`b  [file:]<function>`\
`b  [file:]<line number>` \
Sets a breakpoint at a function or line.

### **Conditional Breakpoint**

`condition <breakpoint-number> <expression>` \
Adds a condition so that the breakpoint only stops execution when the condition is true. Remember that you need to add a normal breakpoint first and then add a condition on top of it.

### **Delete Breakpoint**

`delete [breakpoint-number]`\
Self-explanatory.

---

## Inspecting Variables

### **Print**

`print <expression>`\
`p <expression>` \
Prints the current value of a variable or expression.

### **Call**

`call <function>(args)` \
Invokes a function manually while debugging (useful for testing behavior interactively). Keep in mind that this will not work with functions defined with `auto` or `std::function`.

### **Watch**

`watch <variable>` \
Stops execution/prints a message whenever the variable’s value changes.

### **Display**

`display <expression>` \
Automatically prints the value of the expression each time the program stops.

---

## Handling Recursion

### **Backtrace**

`bt` \
Shows the call stack (useful for viewing recursion depth or nested calls).

### **Up / Down**

`up [n]`\
`down [n]` \
Moves the context up or down `n` stack frames to inspect different levels of the recursion or call hierarchy.

### **Frame**

`frame <n>`\
Directly goes to the `n`-th stack frame. The frames are numbered deep first, that is, the deepest call gets the frame number 0.

---

## Inspecting Function Context

These commands are extremely useful for debugging functions.

### **Info Arguments**

`info args`\
Displays all arguments passed to the current function (that is, the selected stack frame).

### **Info Locals**

`info locals`\
Displays all local variables in the current function (those defined inside the function body).