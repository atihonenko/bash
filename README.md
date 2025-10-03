# bash

##### Task 1. Working with files and directories
```bash
touch bash1.txt                       # First, create a file named bash1.txt where you will add the executed commands
cd ~                                  # Open your home directory via the terminal
pwd                                   # Determine the name of the folder you are currently in
mkdir test1                           # Create a directory named test1 inside this folder
cd test1/                             # Navigate into the test1 directory
touch 1.txt 2.txt 3.txt               # Create files named 1, 2, and 3 inside the test1 directory
ls                                    # Check the contents of the test1 directory
cd ~                                  # Navigate back to the home directory
mkdir test2                           # Create a directory named test2 inside the home directory
rmdir test2                           # Delete the test2 directory
cd test1/                             # Delete file 2 from the test1 directory
rm 2.txt                     
cd ~                                  # Create a directory named test3 in the home directory and add two files to it
mkdir test3
touch 1.png 2.png                                
cd ..                                 # Delete the test3 directory                       
rm -R test3                  
mkdir test4                           # Create a directory named test4 in the home directory
mv test1/1.txt test4                  # Move files 1 and 3 from the test1 directory to the test4 directory
mv test1/3.txt test4          
echo line >> 1.txt &&                 # Add three lines containing the word "line" to file 1
echo line >> 1.txt &&
echo line >> 1.txt 
cat 1.txt                             # View the contents of file 1
echo line >> 3.txt                    # Add three lines containing the word "line" to file 3
echo line >> 3.txt                    
echo line >> 3.txt 
cat 3.txt 1.txt                       # View the contents of both files (1 and 3) at the same time
nano 1.txt                            # Using a text editor, replace all lines in file 1
```
##### Task 2. Editing files, checking and killing proccesses, pinging websites
```bash
touch bash2.txt                                    # First, create a file named bash2.txt where you will add the executed commands
cd ~                                               # Go to the home directory via terminal
mkdir test3                                        # Create folder test3
echo -e "row1\nrow2\nrow3\nrow4" > test3/4.txt     # Add file 4.txt with 4 lines to folder test3
echo -e "row1\nrow2\nrow3\nrow4" > test3/5.txt     # Add file 5.txt with 4 lines to folder test3
echo -e "row1\nrow2\nrow3\nrow4" > test3/6.txt     # Add file 6.txt with 4 lines to folder test3
grep "row2" test3/5.txt                            # Find line row2 in file 5
grep -r "row" test3/                               # Find line row in folder test3
grep -c "row" test3/6.txt                          # Count how many lines with content row in file 6
find test3/ -name "5.txt"                          # Find file 5 inside folder test3
find test3/ -name "5.txt" -delete                  # Using find command, delete file 5
echo "test" >> test3/4.txt                         # Using echo command, add word test to file 4
sed -i 's/test/fail/g' test3/4.txt                 # Replace word test in file 4 with fail
echo "test" >> test3/4.txt                         # Add word test to file 4 while preserving existing content
ps aux                                             # View all processes for users not only in console that are happening in the system
kill [PID]                                         # Kill any unimportant process in console
ping rusau.net                                     # Check availability of resource rusau.net using ping
ping -c 5 rusau.net                                # Send 5 packets to site rusau.net
curl -X GET "https://petstore.swagger.io/v2/       # Get information about registered pets with any status
pet/findByStatus?status=available"                                
curl -X POST "https://petstore.swagger.io/v2/      # Create a new user 
user" -H "Content-Type: application/json"
-d '{"id": 1, "username": "testuser", "firstName":
"Test", "lastName": "User", "email": 
"test@example.com", "password": "password",
"phone": "123456789", "userStatus": 1}'
```
