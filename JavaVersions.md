# Java Versions

Changing Java versions is not exactly the most intuitive process. 
The following are some tips which are often overlooked in popular guides or forum answers about this matter.  

Start by checking you have the following system environment variables:

- JAVA_HOME set to the directory of your java version (e.g. `C:\Program Files\Java\jdk-16.0.0`)

- Path with an entry of `%JAVA_HOME%\bin` before `%SystemRoot%\system32`
(as well as `C:\Program Files\Common Files\Oracle\Java\javapath`, if present)

Then to avoid possible conflicts ensure that there are no java related user variables.


Finally, you can verify the precedence in selecting java versions by running:

```where java```

Which might return something like

```
C:\Program Files\Java\jdk-16.0.0\bin\java.exe
C:\Program Files\Common Files\Oracle\Java\javapath\java.exe
C:\Windows\System32\java.exe
```

## Remember To:
- Close and restart the terminal before checking if the changes have been successful
- JAVA_HOME is usually used by scripts and other commands like `mvn`
- Path is used by `java` and `javac` commands