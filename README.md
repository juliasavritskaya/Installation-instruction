/****** by mnkqn******/

All the following instructions are for OS Windows 10.

**0) Download the file**


**1) Java and JDK installation**
   
1.1. Check if Java is installed on your computer:
    
- Open command line (win +r and "cmd" in dialog box).
- Enter java -version.
- Enter javac -version.  
   
If Java and JDK is installed, expected result is as followng: ![image](https://user-images.githubusercontent.com/55387479/119819735-5eb53480-bef9-11eb-8836-d49fe68c1ca2.png)
    
If Java is installed go to p.2
  
If Java is not installed:
    
1.2 Go to https://www.oracle.com/java/technologies/javase-jdk16-downloads.html (or search for newest Java version by googling "Jdk download")
    
1.3 Select suitable option for your OS. We are using Windows x64 Installer    
    
1.4 Follow the inctructions of Installer. Recommended directory for jdk setup is C:\Program Files\Java\jdk_version_
⠀    
⠀    
 ⠀   
**2) Setup environment variables (Java home)**

   - In search enter "environmental variables" and select suitable option.
    
   - Click "edit".
    
   2.1 Under System Variables, click New.
    
   - In the Variable Name field, enter JAVA_HOME.
   
   - The value for variable is the path to jdk folder (e.g. C:\Program Files\Java\jdk-16).
   
   - Click OK and Apply Changes.
   
   2.2 Under System Variables, choose PATH variable.
   
   - At the end of the value for variable enter the path to jdk bin folder (e.g. C:\Program Files\Java\jdk-16\bin).
   
   - Click OK and Apply Changes.


**3) Check if Java is installed properly:**
   
   - Open command line (win +r and "cmd" in dialog box).
   
   - Enter java -version 
   
   - Enter javac -version.
   
   - Enter echo %JAVA_HOME%
  
  Expected result is as followng (version of java and javac is displayed, path fot jdk folder is displayed for JAVA_HOME):
    ![image](https://user-images.githubusercontent.com/55387479/119828185-9aa0c780-bf02-11eb-8870-a9c0d205ca28.png)

 ⠀  
 ⠀  
   ⠀
**4) Compiling code with cmd**
   
  4.1 
  - Open command line (win +r and "cmd" in dialog box).
  
  - Go to directory where file with code is located using cd command ( e.g. cd D:\Java projects\Task1).
  
  - Enter javac FileName.java (e.g. javac Task1.java or javac by\savritskaya\task1\Task1.java if file is in some package) .
 
 If everything is right, file with .class extension should appear in the same directory.
 
 If everything is not right - use Google. I know you're smart enough.
 
 4.2 
 Enter java FileName in command line (e.g. java Task1 or java by.savritskaya.task1.Task1)
   
  ![image](https://user-images.githubusercontent.com/55387479/119829181-a5a82780-bf03-11eb-88ef-fd778b2648a1.png)

⠀
⠀    
  ⠀  
**5) Compiling code with .jar**
  
  5.0. Do p. 4.1.
  
  5.1. Create .jar file:
 
 - Open command line (win +r and "cmd" in dialog box).
  
 - Enter command:     
   
        jar cfe YourJarFileName.jar PackageDirectory.YourMainClassName PackageDirectory/YourMainClassName.class
        
    In our case it is:
    
        jar cfe Task.jar by.savritskaya.task1.Task1 by/savritskaya/task1/Task1.class
    
  5.2 Compile .jar file:
  
   In the same directory, use command line command:
   
    java -jar JarFileName.jar
 
   
  In our case it is:
            
    java -jar Task.jar
   ⠀ 
    ⠀
    ⠀
  **6) If you're crazy enough, you can also create a .bat file, so you can just double-click on it and launch our incredible application, but that's a completely different story (and I believe you're mentally stable enough so plz don't make me do it)**   
