# TestVagrant Validation project
Higlight : IMDB release date and country  vs Wikipedia release date and country validation
Input movie name : Pushpa the rise
Environment Setup : Maven used as a build management tool To maintain a proper folder structure and add  a dependency what i want this project particularly.
When add a dependency its converts automatically into jar  file . selenium (3.141.59) Webdriver used as a automation tool here with java (1.8) as a programming language implemented tool Eclipse IDE.
In eclipse created a project as Testvegrant and created a proper folder for Base class ,Filereader,pom in Src/main/java and runner class in src/test/java.Then add a dependency and TestNg library because i used TESTNG framework here.
Now in Runnerclass started to write a automation script using a java with selenium .
After finish the script  i started  to customize my project such as ..
Baseclass contains the all reusable method including browser setup and its methods
In pom contains two class one is for IMDB another one is for Wikipedia where i collect the all webelement and stored separatley make it as private because we avoid the confilict between common webelement.when we create a object for pom class in runner class in invoke the constructor in pom class with the help of pagefactory we can access and implement the pom objects in runnerclass.
I stored the URL and Input name in configuration.proprties file which is placed in src/main/java Testvagrantconfiguration package.Using singleton Design pattern i implemented this in my runner class. In SDP there is two class used one for read the properties file and get data another one for manage the reader and get data give into runnerclass.
In Runner Class using extends keyword i inherit the methods from baseclass and implement into my runner class.
create object for POM in runnerclass and customize my script(code).
I took releasedate and country from IMBb and wikipedia website correspondingly and stored in String make it as a public static in class level.I collect four details vice versa..
Using testNg annotation @Test here and also use priority for customize my execution
Here two @Test  method for IMDB_Data and WIki_Dta & @Test(priority=1) for Validation and @Afterclass for browserclose
After i runwith Testng two test cases are pass and one is failed because expected release date is mismatch.
