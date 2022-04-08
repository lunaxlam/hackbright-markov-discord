PROGRAM SET-UP:

Step 1: On Discord - Create a Bot 
- log onto the discord website: https://discord.com/
- navigate to Developer Portal Applications: https://discord.com/developers/applications 
- name your application and click "Create"
- navigate to the "Bot" section and click "Add Bot". Confirm bot creation
- give bot a contextually memorable and fun username
- save your bot's authentication token

Step 2: In VS Code
- create a shell script named "secrets.sh"
- in secrets.sh, create a DISCORD_TOKEN environment variable and set it = to the bot's authentication token

    Syntax:

    export DISCORD_TOKEN="botAuthenticationTokenValueGoesHere"

- create a a file named ".gitignore" and add the following:

    secrets.sh
    *.pyc
    env

- initialize a git repo, make an initial commit, and push your change to GitHub

Step 3: Installing Project Dependencies
- start a virtual environment session with the following command:   virtualenv env
- activate the virtual environment:    source env/bin/activate
- install discord.py with the following command:    pip3 install discord.py
- generate requirements.txt     pip3 freeze > requirements.txt
- add requirements.txt to git repo, commit, and push

Step 4: Connect Bot
- back at Discord Developer Portal Application page, navigate to "OAuth2"
- click on "URL Generator" and find "Scopes"
- click on the box for "bot"
- navigate to "Key Permissions" and select "Send Messages" (write messages) and "Manage Messages" (read messages)
- scroll down and click "Copy" to generate URL
- open URL in new browswer window
- select server to join
- click "Authorize"

Step 5: Running Program
- make sure you pass a .txt file in the command line as argv[1]
- make sure you run the following command in order to access the contents of secrets.sh:

    source secrets.sh 

RUNNING A SESSION:

Step 1: Set-Up Virtual Environment
- start a virtual environment session with the following command:   virtualenv env
- activate the virtual environment:    source env/bin/activate
- install discord.py with the following command:    pip3 install discord.py

Step 2: Prepare "secrets.sh"
- create a shell script named "secrets.sh"
- in secrets.sh, create a DISCORD_TOKEN environment variable and set it = to the bot's authentication token

    Syntax:

    export DISCORD_TOKEN="botAuthenticationTokenValueGoesHere"

Step 3: Running Program
- make sure you pass a .txt file in the command line as argv[1]
- make sure you run the following command in order to access the contents of secrets.sh:

    source secrets.sh 