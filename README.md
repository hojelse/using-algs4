# Using algs4

## Windows and Java

### Option 1 - terminal command with manual classpath

With this option you need to reference `algs4.jar` every time you want to run your program, using the command `java -cp algs4.jar myfile.java`

#### 1. Folder structure

Place MyProgram.java and algs4.jar in the same folder, or maybe place algs4.jar in a library folder like this:

```
my_ADS_programs/
├─── lib/
│    └─── algs4.jar
├─── MyProgram.java
```

#### 2. Import from algs4
Add this line to the top of your MyProgram.java file `import edu.princeton.cs.algs4.*;` to import all algs4 classes.

Or import just one class like `ìmport edu.princeton.cs.algs4.UF;`

#### 3. Execute your program
Use the command `java -cp algs4.jar MyProgram.java` if they are in the same folder.

or change the path to `lib/algs4.jar` if you created a lib folder e.g.: `java -cp lib/algs4.jar MyProgram.java`

### Option 2 - terminal command with global classpath

If you want to be able to import algs4 classes in any java file anywhere on your computer (globally), and use terminal command: `java myfile.java`, try this option.

#### 1. Add the variable `CLASSPATH` to Enviroment Variables:

Navigate to Enviroment Variable on Windows 10 `Control Panel > System and Security > System > Advanced System Settings > Advanced > Environment Variables`

In the example below, replace `\path\to\jdk-1.2.3.4` with your actual path to your [java jdk](https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/latest)

Variable                | Value    
------------------------|----------
CLASSPATH               |   C:\path\to\algs4.jar
JAVA_HOME               |   C:\path\to\jdk-1.2.3.4\
path                    |   C:\path\to\jdk-1.2.3.4\bin\ *;some_other_unrelated_paths_you_shouldn't_mess_with*

The variables, *JAVA_HOME* and *path*, might already be set after installing java jdk.

#### 2. Import from algs4
Add this line to the top of your MyProgram.java file `import edu.princeton.cs.algs4.*;` to import all algs4 classes.

Or import just one class like `ìmport edu.princeton.cs.algs4.UF;`

#### 3. Execute your program

Use command `java MyProgram.java`

## VS Code and Java

If you want to use a light weight IDE, as an alternative to IntelliJ, you might want to try VS Code

#### 1. Install [VS Code](https://code.visualstudio.com/)

#### 2. Create a folder structure

You can create a folder structure with:
1. a `lib/` folder for algs4.jar
2. a `.classpath` file with simply a single line `lib`

e.g.:

```
my_ADS_programs/
├─── lib/
│    └─── algs4.jar
├─── MyProgram.java
├─── .classpath
```

#### 3. Install [java extension pack](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)

After installing, now you should get IntelliSense (code suggestions) within VS Code and you can use the UI or `F5 key` (default keybinding) to run your java program.

**If you get no IntelliSense**

Try this in VS Code, press `ctrl+shift+p` and select the command `Java: Clean Java Language Server Workspace`.

**If VS Code doesn't recognize `import edu.princeton.cs.algs4.*;`**

make sure algs4.jar is under *referenced libraries* in the *java projects* tab in the explorer, like the image below. This will add a *.vscode* folder containing a file containing some pointer to the jar.

![vscode.png](readme-images/vscode.png)







