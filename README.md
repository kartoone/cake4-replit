# installing cakephp4 into repl.it
# steps and notes

Create a new repl.it and search for the php – web server template
Click the shell window and copy/paste the following: composer create-project --prefer-dist cakephp/app:4.* bulldogbot
Press enter at the prompt to select the php80.out composer version
Press enter one more time during the installation to set the folder permissions correctly
Type the following into the shell: cd bulldogbot and press enter
Click the vertical triple dots next to files and select “Show Hidden Files”
Open the file named replit.nix
Change line #4 from pkgs.php74 to pkgs.php80 
(in other words, just change the 74 to 80)
Back in the shell: type the following: php -version
If it still says php7.4, then press the up arrow key and press enter to run the command again
Then type the following and press enter: bin/cake server -H 0.0.0.0

## Add support for the run/stop button
Note that you can make the Run button work by clicking on triple dots and showing hidden files
Then open .replit and change the RUN entry to the following:

run = "bulldogbot/bin/cake server -H 0.0.0.0"

## Add support for unit testing
composer require phpunit/phpunit

## More reading
https://book.cakephp.org/4/en/development/testing.html