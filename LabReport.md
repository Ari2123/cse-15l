# Remote Access

This blog post will be a tutorial for incoming CSE-15L students regarding remote access through Visual Studio Code. 

1. Step #1: **Installing VScode**

Go on the visual studio code website and download it for your appropriate operating system. Once downloaded, it should look something like this:

![Image][1]

[1]: https://ibb.co/fdXmPzn

2. Step #2: **Remotely Connecting**

In order to remotely connect, you will first have to go to https://sdacs.ucsd.edu/~icc/index.php in order to look up your username for the respective
and change your password. Once that is done, you will go on VS code, open a new terminal and paste "$ ssh cs15lwi22zz@ieng6.ucsd.edu" where
the "cs15lwi22zz" will be your specific username. After that you will have to type in your password in order to connect to the remote server.
Once that is done, it should look something like this:

![Image][2]

[2]: https://ibb.co/BrQcjBv

3. Step #3: **Trying Some Commands**

Next step is to try some commands such as "ls -a", "-a", "ls", "ls -i" and see what these commands do. The following is what the two commands ("ls -i" and "ls") that I used give:

![Image][3]

[3]: https://ibb.co/0CbgnPK

4. Step #4: **Moving Files with scp**

For this step you will have to create a file on your computer called "WhereAmI.java" with some contents. After that, open your terminal and run the following:
"scp WhereAmI.java cs15lwi22zz@ieng6.ucsd.edu:~/" This will prompt you for your password which you should input. After that, log into ieng6 with ssh again, and use ls and you will see the files in the home directory. In this step I personally had an issue since my password was being denied which is why this is what it looked like for me:

![Image][4]

[4]: https://ibb.co/ydzvpP5


5. Step #5: **Setting an SSH Key**

The point of this key is to give us the ability to login without the tedious requirement of typing our password each time. You should input "ssh-keygen" in the terminal and receive a series of questions which you will type answers too. Once that is done you will have 2 unique keys: a public and private key. Copy the public key in the ssh directory by using scp. Once that is finished, we are able to login without our password. 

![Image][5]

[5]: https://ibb.co/ZdR3RL6

6. Step #6: **Optimizing Remote Running**

Now we will optimize this process for our personal convenience. I personally did this by the command scp WhereAmI.java cs15lwi22aqi@ieng6.ucsd.edu; ssh cs15lwi22aqi@ieng6.ucsd.edu "javac WhereAmI.java; java WhereAmI". For this step my password was being denied again which is why there is no screenshot. 




