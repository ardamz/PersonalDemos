# Shell Scripting Project

 ## 1.  **Linux**

> I utilised AWS EC2 as my server for this project.

I created and navigated to the `shell` directory by running the following command

```bash
mkdir shell && cd shell
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/main/1.%20Project%201%20LAMP%20Stack%20Implementation/Update%20package%20manager.png)

I the created and populated a `names.csv` file by running

```bash
vim names.csv
```

![Screenshot](https://code1.png)

I then proceeded to created the developers group by running the command below

```bash
sudo groupadd developers
```

![Screenshot](https://code2.png)

I then navigated to `.ssh` directory by running 

```bash
cd ~/.ssh
```

I then created and populated the `id_rsa` and `id_rsa.pub` files by running the `touch` and `vim` command.

I also saved a copy of the private key as `.pem` file locally. This would be used to login as any of the created users using SSH.

```bash
touch id_rsa id_rsa.pub
```

```bash
vim id_rsa.pub
```
```bash
vim id_rsa
```
 ## 2. **Automation Script**

I navigated back to the `shell` directory and created a shell script called `onboarding.sh`. The script will perform the following tasks;

1. Read the `names.csv` file, create each user on the server, and add to the existing group called `developers`.

1. Check for the existence of the user on the system, before it will attempt to create it.

1. Ensure that the user that is being created also has a default home folder

1. Ensure that each user has a `.ssh` folder within its HOME folder. If it does not exist, it creates one.

1. For each user’s SSH configuration, create an authorized_keys file and  ensure it has the public key of my current user.

```bash
cd ~/shell
```

```bash
vim onboarding.sh
```
![Screenshot](https://onboard.png)

I then changed the pemission of the `onboarding.sh` file to make it executable by running the `chmod` command, befor running the script.

```bash
chmod +x onboarding.sh
```

```bash
./ onboarding.sh
```
![Screenshot](https://code3.png)
I was able to get the script to run successfully aftersome initial jitters.


## 3. **Random User Credential Testing**

I was able to use the `su` command to switch to other users within the terminal.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/main/1.%20Project%201%20LAMP%20Stack%20Implementation/Ubuntu%20default%20browser%20page.png)


Using the `Santos.pem` file created earlier, i was able to login as various users on the server.

## 4. **Hiccups**

