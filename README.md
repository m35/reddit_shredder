# Reddit Shredder

Simple script to delete all of your reddit posts and comments, based off a customizable timedelta. This script overwrites your comments with a random string of letters and numbers; overwriting the comment purges it from Reddit's servers. 

# Reddit Shredder Online

I've written an webapp that does the same thing this script does.

https://redditshredder.joshharkema.com/ 

# Requirements

1) Python 2.7 or 3.6.

2) Pip.

# Installation

1) Go here: https://www.reddit.com/prefs/apps/

2) Create a new app (click at the bottom of the page.)
   
   a) Name it whatever you want. 
   
   b) Select "Script."
   
   c) Description and About URL can be blank.
   
   d) Enter 127.0.0.1:8000 into "Redirect URL" (It doesn't matter what you put here, as long as it's a valid URL/IP.)

3) Enter all the info into shredder.py under the main() function. 

4) run:
   
   > pip install -r requirements.txt
   
   and test the script with:
   
   > python shredder.py
   
   
5) If everything works, add a cron script such as:
   
   To run every hour (replace PATH-TO-SCRIPT with correct path):
   
   > 0 * * * * python3 /PATH-TO-SCRIPT/shredder.py
   
   For optional logging:
   
   > sudo touch /var/log/shredder.log
   
   > sudo chmod 600 /var/log/shredder.log && sudo chown root:root /var/log/shredder.log
   
   Then change the crontab line to:
   
   > 0 * * * * python3 /PATH-TO-SCRIPT/shredder.py >> /var/log/shredder.og 2>&1

I'm not sure how a Windows / Mac user could use this script. If anyone has any ideas let me know.
