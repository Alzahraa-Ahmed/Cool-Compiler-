# Cool-Compiler-
  Create compiler for cool programming language

# Prerequisites:
  You need to install antlr4 with your IDE, if you had no information for how to do that follow this [link](https://github.com/antlr/antlr4/blob/master/doc/java-target.md).


# Steps:

  * Click right on Cool.g4 file then select "generate antlr recognizer".
  
  ![setup](https://i.ibb.co/V2RQXSX/Capture.png)
  
  This will generate a set of files in "gen" folder.

  * Move the main file to "gen" folder.
  
  * Change the project src folder from src to gen.
  from menu choose : file >> program structure >> Modules >> sources
  
  ![setup](https://i.ibb.co/DR7Xsrn/Capture.png)

  * Now we should compile our project. 
   right click on any file on gen folder then select "open in terminal".
   write in the terminal the following command:
   
   >javac Main.java CoolBaseListener.java CoolBaseVisitor.java CoolLexer.java CoolListener.java CoolParser.java CoolVisitor.java

# NOTE Before Running
  - You should run Main from terminal as it accepts the file as argument like 
  >java Main.java "testCases/bad.cl"
  
  * run the project.

# Compiler structure: 

  compiler is divided into few sequential steps: lexical analysis, parsing, semantic rules, three address code generation.

## Lexer:

   Define the language terminals throughout some [regex](https://www.rexegg.com/regex-quickstart.html).

   Here there are 2 files in folder testCases to test the lexer one with good terminals and one for bad.
  
### Input: 

  file.cl
  
### Output:

  file-lex.txt
  
  here is the output for our test cases : 
  
  for [good](https://github.com/Wafaaismail/Cool-Compiler-/blob/master/good.cl-lex)
  
  for bad it won't produce a file so this is the output
  
  ![result1](https://i.ibb.co/V9r4TTk/Capture.png)
  
## Parser:
  
  Define the grammer of COOL in [Cool.g4](https://github.com/Wafaaismail/Cool-Compiler-/blob/master/src/Cool.g4) file.
  
  To test the grammer, there's a program which checks whether the number is a palindrome or not written in COOL. 
 
### Input:

  file.cl
  
### Output:

  For right code, it will produce the parse tree of this code.
  
  For wrong one, it will show the error in the file and where it's.
  
  * The parse tree for the for [goodParser.cl](https://github.com/Wafaaismail/Cool-Compiler-/blob/master/testCases/goodParser.cl) example:
  
  ![result](https://i.imgur.com/WcXw5UQ.png)
  
## Semantic rules:

## 3 address code generation:


  
