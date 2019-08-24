# Type-Based-Package-Dependency-Analysis

This project mainly focuses on a part of a code analyser that is a Dependency analyser based on type based package.
To perform the dependency anaylsis I have built :
 1) Typetable which stores the type information for a particular package.
 2) TypeAnalysis : Finds all the types defined in each of a collection of C# source files. 
 It does this by building rules to detect type definitions - classes, structs, enums, and aliases.
 3) DepAnalysis : Finds, for each file in a specified collection, all other files from the collection on which they depend. 
 File A depends on file B, if and only if, it uses the name of any type defined in file B. 
 It might do that by calling a method of a type or by inheriting the type.
 Note that this intentionally does not record dpedndencies of a file on files outsied the file set, e.g., language and platform libraries.
 4) StrongComponent : A strong component is the largest set of files that are all mutually dependent. 
 That is, all the files whcih can be reached from any other file in the set by following direct or transitive dependency links.
 The term 'Strong Component' comes from the theory of directed graphs. 
 There are a number of algorithms for finding strong components in graphs.
 My favorite is the Tarjan Algorithm, nicely described here: Tarjan Algorithm and pseudo code. 
 You will need a graph class to implement this. 
 5) Display : Uses information in the TypeTable to build an effective display of the dependency relationships 
 between all files in the selected collection. Note that you are not expected to provide a graphical display.
 An indented text display will satisfy these requirements.
 6) Tester : Provides code to demonstrate you meet all requirements.
 
 
 # Install this project in your system
 You will need Visual Studio 2015.
 The project consists of run.bat and compile.bat files. 
 Run.bat - Runs the project. It is required for C# or VB.NET applications.
 Compile.bat - Compiles the project automatically. 
 Execute run.bat and compile.bat on your command propmpt to run this project.
 
