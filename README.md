# pwm
Simple to use local password manager for hackers. everything is encrypted and stored on your file system.
pwm is a one bash script that uses `zernity` for displaying windows, `bash` and `awk` for text formating and `openssl` for encryption.


#### Requirements:
- bash - the default shell on most Unix systems
- awk - installed by default on most Unix systems
- openssl - installed by default on most Unix systems
- zenity - installed by default on some Unix systemns. if not `apt install zenity` , `dnf install zenity`


#### How it works?:
Simply pwm takes your account name and password, encrypte the password and store the data in the file `${HOME}/.passwd` in `CSV` format. This makes it very easy to share your `.passwd` file between your devices and `pwm` will be able to pick up all new accounts.

> if you're runing `pwm` for the first time and your `.passwd` file is empty, `pwm` will use your first account to decide what your main password will be. Essentially `pwm` tries to decrypt the first account in `.passwd` with your password, if the decryption succeed than it's the correct password.

##### Cammands:
  - `pwm` to search for an account
  - `pwm -l` to list all accounts
  - `pwm -a` to add a new account
> To delete an account, you just need to edit `.passwd` file yourself
![zenity window](https://imgur.com/gT7Q74i.png)
![zenity window](https://imgur.com/PreYKeB.png)
