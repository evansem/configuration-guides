# Useful Eclipse IDE set-up 💻

This is often used for Software Engineering courses at Victoria University of Wellington, 
Hence the following notes can beneficial in particular for students taking:
- Swen221
- Swen225
- Swen326

### How to import a template code from  jar file 🏗️

- Right Click on the project folder
    - Import → Archive (for source file)
    - Build Path → Add External Jar (library)
    - Build Path → Configure Build Path → Library Tab → Add Library → Junit
    - Build Path → Configure Build Path → Library Tab → Add Library → JRE System Library
        - For ECS machines if it is not 11 go to Installed JREs
        - Then select ```/usr/pkg/java/adoptopenjdk11-bin```

    - hover Build Path → mark ```src``` as source dir
    
### Assertions

Instructions like ```assert myVar != null;``` are not being check by default.

It is required to enable them, you can do this by clicking:

1. The green play button :arrow_forward:
2. Run Configuration
3. *Arguments* tab
4. VM arguments
5. Enter the value ```-ea```

### General Trouble Shooting ⚠️

1. First of all try deleting module info
2. Then if it has been compiled by a more recent version of the Java Runtime → needs newer JDK
3. At the time I am writing the university is reccomending to use java 11

### How to configure @NotNull annotation

1. Scroll to an instruction containing @NonNull
2. hover the mouse on it
3. Select *Copy Build Path to Library*

### Enable all warning and null analysis ✔️

1. Right Click on the project folder
2. Select properties
3. java Compiler
4. Errors/Warning
5. Then turn on all to errors 
6. Remeber to scroll maximise the different sections using the downwards arrow 🔽 
Null analysis is at the bottom of the same tab


### JUnit 5 test exceptions

assertThrows(NoSuchRecordException.class, new StudentManager().readStudent("0"));

[Check out this link for other possible ways](https://blog.aspiresys.pl/technology/different-ways-of-testing-exceptions-in-java-and-junit/)

