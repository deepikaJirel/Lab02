## Lab 02

- Name: Dipika Jirel
- Email: jirel.2@gmail.com

## Part 1 Answers

1. Command & steps to create an SSH key pair:</br>
       `ssh -i ./labuser.pem ubuntu@44.217.99.208`</br>
       ` ls `</br>
       `chmod labuser.pem 600`</br>
       `Chmod 600 ./labuser.pem`</br>
       `ssh-keygen -t ed25519`</br>
       `ls`</br>
       `ls -lah`</br>
       `cd .ssh`</br>
       `ls`</br>
       `vim id_ed25519.pub`</br>
       `cat id_ed25519.pub`</br>
       `cd ceg2350-dipikajirel`</br>
       `ls`
2. Steps to add public key to GitHub profile:
       After generating the public key </br>
       - login to `GitHub`.</br>
       - go to `setting`</br>
       - click on `SSH and GPG keys`</br>
       - click on `Add new SSH Key`</br>
       - Add title make sure you put the Key Type as `Authentication key` and paste the key that you got from `AWS Ubuntu instance` and click on `Add SSH key`</br>
3. git command to clone the repository: 
       `git clone >repository_url>`</br>
        for example ` git clone https://github.com/deepikaJirel/ceg2350-dipikaJirel.git`
  
## Part 2 Answers

The answers for this section are to help you record what steps  
are needed to create a file locally (in your cloned repo)  
and push them (sync) with GitHub.  Only `git` commands are 
valid answers

1. git command to view the status of the repository: </br>
       ` git status`
2. git command example to add a file for tracking: </br>
    `git add <file_name>`
3. git command to commit changes: </br>
    `git commit -m "type a message"` 
4. git command to sync local commits with GitHub: </br>
    `git push origin <branch-name>`
5. git command to sync commits on GitHub to `clone`d repository: </br>
    `git pull origin <branch-name>`


## Part 3 Answers

1. `chmod u+r bubbles.txt`
    - Means:</br>
       the command `chmod u+r bubbles.txt` permits the user to read the .txt file. It remains the same if the user already has permission to read it. 
                                   
2. `chmod u=rw,g-w,o-x banana.cabana`
    - Means: `The user will have read and write permission, The group will have no write permission others will have no execute permission while the read, write permission is unaffected and the banana.cabana file that we are modifying.`
3. `chmod a=w snow.md`
    - Means: `This command sets the permission for all the users who only have to write on the file snow.md. `
4. `chmod 751 program`
    - Means: `This command gives the user full permission to read, write and execute. The group reads and execute permission and others only execute permission.`
5. `chmod -R ug+w share`
    - Means: `The command share recursively grants write permission to the user and the group for the directory share and all files and subdirectories within it.`      

## Part 4 Answers

1. Command to create new user: </br>
       `sudo useradd <username>` `For example: sudo useradd djirel`
2. Path to user's home directory: </br>
       `/home/<username>` `For example: /home/djirel`
3. Evaluate if `ubuntu` can add files to user's home directory:</br>
       `ls -ld /home/<username>` `For example: ls -ld /home/djirel`
4. Command to switch to user:</br>
       `su - <username>` `For example: su - djirel`
5. Command(s) to go to user's home directory:</br>
       `cd /home/<username>` `for example: cd /home/djirel`
6. Evaluate if user can add files to user's home directory:</br>
       `ls -ld /home/<username>` `for example: ls -ld /home/djirel`
7. Command to switch to `ubuntu`:</br>
       `su - ubuntu`
8. Command to return to `ubuntu` home directory: </br>
       `cd /home/ubuntu`

## Part 5 Answers

For each, write the command used or answer the question posed.

1. Command to create group named `crew`:</br>
       `sudo groupadd crew`
2. Command(s) to add `ubuntu` & user to group `crew`:</br>
       `sudo usermod -aG crew ubuntu`
       `sudo usermod -aG crew djirel`
3. Command to modify `share` to have group ownership of `crew`:</br>
       `sudo chown :crew /path`  we need to replace /path with the actual path.
4. Command to switch to user:</br>
       `su djirel`
5. Command to add file to `share`:</br>
       `touch share/fileName.txt`

6. Evaluate why these steps allowed the above action:</br>
   `These steps collectively ensured that the necessary permissions and ownership settings were in place, allowing users in the crew group to manage files within the share directory effectively.`

## Part 6 Answers

For each, write the command used or answer the question posed.

1. Command to create a file using `sudo`:</br>
       `sudo touch filename`
2. Evaluate (in plain text) the permission of the file: </br>
       `ls -l /pathOfTheFile`
3. Provide a method to edit the file without modifying permissions: </br>
       `sudo vim /pathOfTheFile`
4. Command(s) to modify permissions:</br>
       `chmod 755 /pathToDirectory`
   The above command gives the user read, write, and execute permissions, read and execute permissions to the group and others.

