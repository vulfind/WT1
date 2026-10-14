# WT1  

PHP PRACTICAL 3 - COMMANDS AND STEPS
====================================

PART 1: CHECK AND INSTALL PHP
-----------------------------
Step 1. Check whether PHP is installed:
        php --version

Step 2. If Step 1 shows "command not found" or an error, install PHP:
        sudo apt install php

PART 2: GO TO THE WEB FOLDER
----------------------------
Step 3. Move to the web root folder:
        cd /var/www/html

PART 3: CREATE THE PHP FILE
---------------------------
Step 4. Create and open the file in the nano editor:
        sudo nano simple.php

Step 5. Type your code (sample below).

Step 6. Save the file:
        Press Ctrl+O, then press Enter.

Step 7. Exit nano:
        Press Ctrl+X.

Note: The file name MUST end in .php (for example simple.php).
      PHP does not run .html files.

SAMPLE CODE (simple.php)
------------------------
<!DOCTYPE html>
<html>
<head>
    <title>PHP Practical 3</title>
</head>
<body>
    <h1>Output:</h1>
    <?php echo "Hello from PHP!"; ?>
</body>
</html>

Rules to remember:
- PHP code goes between <?php and ?>
- Use echo to print output inside the HTML
- End each PHP statement with a semicolon ;

PART 4: RUN ON THE LOCAL SERVER
-------------------------------
Step 8. Stay in /var/www/html and start the PHP built-in server:
        php -S localhost:8080

        Keep this terminal open while the server runs.

Step 9. Open Firefox and go to:
        http://localhost:8080/simple.php

Step 10. Check the output on the page.

Step 11. Stop the server:
        Go back to the terminal and press Ctrl+C.

OPTIONAL: USING index.php
-------------------------
If you name the file index.php instead, you can open the page with just:
        http://localhost:8080

QUICK REFERENCE (ALL COMMANDS IN ORDER)
---------------------------------------
php --version
sudo apt install php
cd /var/www/html
sudo nano simple.php
        (type code, Ctrl+O, Enter, Ctrl+X)
php -S localhost:8080
        (open http://localhost:8080/simple.php in Firefox)
        (Ctrl+C to stop the server)

NANO EDITOR SHORTCUTS
---------------------
Ctrl+O   Save (write out) the file
Enter    Confirm the file name when saving
Ctrl+X   Exit nano

TROUBLESHOOTING
---------------
Problem: "command not found" for php
Fix:     Run: sudo apt install php

Problem: "Permission denied" when saving
Fix:     Open the file with sudo: sudo nano simple.php

Problem: Browser shows the code instead of the output
Fix:     Check that the file name ends in .php
         Check that the URL starts with http://localhost:8080
         (Do not open the file directly by double-clicking it)

Problem: Blank page or error message
Fix:     Check that <?php and ?> are correct
         Check that each statement ends with ;
         Check the terminal for error messages

Problem: "Address already in use" when starting the server
Fix:     Use another port, for example: php -S localhost:8081
         Then open http://localhost:8081/simple.php

Problem: Page not found (404)
Fix:     Make sure you ran the php -S command from /var/www/html
         Make sure the file is saved in /var/www/html
