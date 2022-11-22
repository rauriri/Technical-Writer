# How to install JBoss EAP

Download the installer file (jboss-eap-7.3.0-installer.jar) and locate it in a folder with enough permissions. ***/opt*** directory is usually a good place.


- Run this command to start the installation:

    ```console
    /opt$ java -jar jboss-eap-7.3.0-installer.jar -console
    ```

- Select the language when  asked:
    ```console
    Select your language below :
    0: English
    1: 中文
    2: Deutsch
    3: français
    4: 日本語
    5: português
    6: español
    Please choose [0] :
    0
    ```

- Agree with Red Hat license, type 1 and press ENTER:
    ```console
    Copyright (c) 2013 Red Hat, Inc. All rights reserved. Red Hat, JBoss and the JBoss logo are registered trademarks of Red Hat, Inc. All other trademarks are the property of their respective owners.

    press 1 to continue, 2 to quit, 3 to redisplay.
    ```

- Select default installation path, just press ENTER:
    ```console
    Select the installation path:  [/opt/EAP-7.3.0]
    ```

- Choose the modules to install, default options should be good enough:
    ```console    
    Select the packs you want to install:
    1    [x] [Required]      [Red Hat JBoss Enterprise Application Platform] (29.79 MB)
    2    [x]                 [AppClient] (31.89 KB)
    3    [x]                 [Docs] (16.37 MB)
    4    [x] [Required]      [Modules] (184.66 MB)
    5    [x] [Required]      [Welcome Content] (2.1 MB)
    Total Size Required: 232.95 MB
    Press 0 to confirm your selections

    Please select which packs you want to install
    0
    Pack Selection Done
    press 1 to continue, 2 to quit, 3 to redisplay.
    1
    ```

- Create a username and password to admin the server. Please remember to **write it down**, as it will be needed later:
    ```console
    Create an Administrative User
    This user will be added to the host container's management realm for administrative purposes. It can be used to access the management console, the management CLI, or other applications secured in this realm.

    For minimal security, the password should be at least eight characters long, with one alphabetic character, one digit, and one non-alphanumeric symbol excluding "&".


    Admin username: [admin]
    1234

    Admin password: []
    ****
    Confirm admin password: [****]

    Validation error:
    Please enter a password.
    Confirm admin password: [****]
    ****
    Validation warning:
    Username and password cannot match.
    Password should have at least eight characters.
    Password should have at least one alphabetic character.
    Password should have at least one non-alphanumeric symbol.
    press 1 to continue, 2 to quit, 3 to redisplay.
    1
    ```

- Select default server configuration:
    ```console
    Configure Runtime Environment
    There are several additional options for configuring Red Hat JBoss Enterprise Application Platform now that the server has been installed. Each option can be individually chosen, and will be configured in the order displayed upon pressing "Next". What would you like to do now?
    0  [x] Perform default configuration
    1  [ ] Perform advanced configuration
    Input Selection:
    0

    press 1 to continue, 2 to quit, 3 to redisplay.
    1
    ```

- Process will start and server will be installed:
    ```console
    [ Starting processing ]
    Starting process Logging installation information (1/3)
    IzPack variable state written to /opt/EAP-7.3.0/installation/InstallationLog.txt
    Starting process Adding admin user (2/3)
    Starting process Cleanup extraneous folders and tepmorary files (3/3)

    Create shortcuts in the start menu (y/n) [y]:
    n
    Installation has completed successfully.
    Application installed on /opt/EAP-7.3.0

    Would you like to generate an automatic installation script and properties file? (y/n) [n]:
    n
    [ Console installation done ]
    ```

    Please, proceed with the next chapter to **test and configure** JBoss. 

    Continue to [Configuration](CONFIGURATION.MD) section.
    
    [Go back to README.MD](README.md)