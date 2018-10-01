# CSIL-Usage

This repository contains information on how to effectively use the CSIL at UCSB with your own Laptop.

## Logging Into CSIL for the first time

Firstly, we want to be able to log into CSIL. To log into CSIL remotely for the first time type in the following command in terminal:

```
ssh USERNAME@csil-18.cs.ucsb.edu
```

SSH will first ask you a question which looks like this:

```
The authenticity of host 'csil-18.cs.ucsb.edu (128.111.43.14)' can't be established.
RSA key fingerprint is 90:ab:6a:31:0b:81:62:25:9b:11:50:05:18:d3:1a:b5.
Are you sure you want to continue connecting (yes/no)?
```

Type __yes___ and then ___ENTER___ to continue. It will next ask for your CoE account password. When you type it in, nothing will show on the screen (not even dots). However what you type is still being sent and once you are finished with your password, you can press ENTER to login.

You should now be remotely connected to CSIL! You can make sure by typing the following command (which will tell you what machine you are currently issuing commands to):

```
hostname
```

To exit CSIL from your terminal, simply input the following command:

```
exit
```

And to re-enter into CSIL put in the following command:

```
ssh USERNAME@csil-18.cs.ucsb.edu
```

## Creating a macro to log into CSIL (Mac Users Only)

Congratulations on getting into CSIL for the first time. However, in logging into CSIL multiple times it can be annoying to type the same command over and over again. To simplify this, we are going to create a macro to make logging in easier.

So open up your terminal, and navigate to the home directory by typing in:
```
cd
```

Now that we are in our home directory, we want to edit the .bash_profile. So type in the following command:

```
vim .bash_profile
```
___*Note: You can use any editor you want, I just prefer VIM___

Now that we are in our bash profile, we want to create the macro. Copy the following command (replacing USERNAME with your COE account name).

```
csil()   
{         
         
        ssh -X USERNAME@csil-"$1".cs.ucsb.edu
}
```

Now save and exit the file (On VIM its :wq).

You should now be able to connect to CSIL using the command (Subsitution SERVER-Name for a number between 1 and 48):

```
csil SERVER-NAME
```

## Using CSIL Passwordlessly







