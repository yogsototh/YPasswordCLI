> This project has two homes.
> It is ok to work in github, still, for a better decentralized web
> please consider contributing (issues, PR, etc...) throught:
>
> https://gitlab.esy.fun/yogsototh/YPasswordCLI
# YPassword

This is the YPassword command line utility. 

YPassword is password management method. 
It helps you to use only very strong password everywhere. 
Each different for each website.
Accent is made on portability.

To learn more about this method just visit:
[ypassword.espozito.com](http://ypassword.espozito.com)

It needs you to create a ~/.password file, it should contains something
similar to:

    forrst.com      yogsototh                10 b64 sha512
    freenode.net    yogsototh                10 b64 sha512
    foursquare.com  yann.esposito@gmail.com  10 b64 sha512 1
    twitter.com     yogsototh                20 hex sha512

Columns:

1. URL of website
2. Login
3. Size of the password
4. Output format b64 (recommended) or hex
    b64 is something like: `NzMzN2Q2ZWFhMDUxYWVlNTcxMTgwYzViM`
    hex is something like: `7337d6eaa051aee571180c5b356d40b4294e4c7242b6e3bc39fc700bab550540`
5. Hash algorithm sha1 (not recommended), sha256, sha512 (recommended)
6. An optional number, if you want to change your password for a specific website, just change this number.

Usage:

    ypassword pattern

The application wait for you to type your main password each time you use it.

Example:

    > ./ypassword twit
    twitter.com (yogsototh): 0018b7bd1cd0197e1ae14dfbc568b27b3a45

In the end you'll only have to copy/paste this password.
