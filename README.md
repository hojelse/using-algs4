# Using algs4

## Windows and Java

### Option 1 - terminal command `java -cp algs4.jar myfile.java` with manual classpath

With this option you need to reference `algs4.jar` every time.

##### 1. Use command `java -cp algs4.jar myfile.java`...
... assuming myfile.java and algs4.jar is in the same folder, and a relative path `algs4.jar`

otherwise you might use a absolute path `java -cp C:\path\to\algs4.jar myfile.java`

### Option 2 - terminal command `java myfile.java` with global classpath

If you want to be able to import algs4 classes in any java file anywhere on your computer (globally), and use terminal command: `java myfile.java`, try this option.

##### 1. Add the variable `CLASSPATH` to Enviroment Variables:

*the variables, `JAVA_HOME` and `value`, might already be set after installing java jdk*

Variable                | Value    
------------------------|----------
CLASSPATH               |   C:\path\to\algs4.jar
JAVA_HOME               |   C:\path\to\jdk-1.2.3.4\
path                    |   C:\path\to\jdk-1.2.3.4\bin\ *;some_other_unrelated_paths_you_shouldn't_mess_with*

##### 2. replace `\path\to\jdk-1.2.3.4` with your actual path to your [java jdk](https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/latest)

##### 3. import from algs4 by adding this line to the top of your .java file `import edu.princeton.cs.algs4.*;`

##### 4. and then use `java myfile.java` to execute your program

## VS Code

If you want to use a light weight IDE, as an alternative to IntelliJ, you might want to try VS Code

Install [java extension pack](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)

You can create a folder structure with:
1. a `lib/` folder for algs4.jar
2. a `.classpath` file with simply a single line `lib`

e.g.:

```
kattis/
├─── lib/
│    └─── algs4.jar
├─── MyProgram.java
├─── .classpath
```

You now should get IntelliSense (code suggestions) within VS Code and you can use the UI and `F5 key` (default keybinding) to run your java program.

**If you get no IntelliSense** try this in VS Code, press `ctrl+shift+p` and select the command `Java: Clean Java Language Server Workspace`.

![vscode.png](readme-images/vscode.png)







