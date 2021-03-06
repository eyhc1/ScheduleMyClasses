# MyUW Exporter
Export your class schedule from MyUW to and .ics file so that one can import it to their calendar app such as Outlook or
Google calendar.

## Use
### Directly use
[Download the .jar file](https://github.com/eyhc1/ScheduleMyClasses/releases) from release to use the program directly. Due to log4j2 security issue, it is highly recommended to download release version 3 and up.
### Develop
Clone this repository into your computer, then open command prompt and direct it to the folder where all the files are
located. Then type `gradlew build` to build the project. If you are using an IDE such as Intellij, it might going to
build it automatically once you opened the project into it. After completing building it you can go to `src` folder to
edit the programs.
### Compile and jar
Type `gradlew jar` in the command prompt which has been directed into the project folder to create a standalone program.
The program .jar file should be created in build > libs directory.
### Optional Arguments (Version 3.0.0 and up)
There are three argumentscan be used when calling the .jar file. Default usage is `java -jar ScheduleMyClasses-VERSIONID
[Option 1]=[value] [Option 2]=[value] [Option 3]`. The three valid options are:  
`-netid`: Your UWNetID, this option typically followed by  
`-password`: The password associated with that NetID account  
`-disable2faDiag`: If Duo 2fa enabled, this option will disable any prompt that will pop up during the login process and
assumed you have your default device nearby and available  
With `-netid` and `-password` can autofill the text field and can be functioned as "remember me" when have the argument 
saved in a batch file.


## Depends
- Java 8
- jsoup 1.10.3
- gson 2.8.7
- jopt-simple 5.0.3
- <s>log4j 2.14.1</s> (very old versions only)

## Old version
This repository was updated from a version that was written in Python. You can check the archived repository [here](https://github.com/eyhc1/visual-schedule-to-ics).

## Issues
- Sometimes the error popup shows nothing
- Some popup message not showing anything messages
- Program crashed when attempting to parse on web in Windows 11
- <s>Not working for 2 Factor Authendication (2FA)</s>

## Todo:
- [ ] Fix Issues
- [ ] Convert final exam schedule as well
- [x] Disable log4j for security
