Committing and Pulling Code
===========================

Once you've finished adding some juicy, fresh touches to the Maps Plugin, it's time to push your changes back to the original Maps Plugin repository.
To do this, you first need to save your changes in what's called a 'commit'. A commit is made up of changes to files in a certain repository.
To create a new commit using the GitHub client for windows or mac, simply open the Maps Plugin repository in the client, make sure your changes appear to the right, and write a short, descriptive summary of your changes in the box on the left.
Then click the 'commit' button, the 'sync' button in the top right and your changes should now appear in your fork on the GitHub site!

[Client Image]

Creating a commit with the [git command-line client]() is slightly more tricky. To commit your changes using the command-line, open up a new terminal or command prompt window.
Navigate to the repository on your computer using ```cd C:\Users\psgs\Documents\GitHub\MapsPlugin```, where 'C:\Users\psgs\Documents\GitHub\MapsPlugin' is the path to your local repository.
From there, execute the command ```git add .```, then ```git commit -m "Commit Message"```, where 'Commit Message' is a short description of the changes to the code you've made. Don't forget the quotation marks around your description.
Once that's done, the last command you need to execute is ```git push origin master```, which will synchronise your local copy of the repository with the copy on the GitHub site.

To add your changes to the main Maps Plugin repository, navigate to your fork of the repository on the [GitHub site](http://github.com) and click on the 'pull requests' link in the bar on the right.

[Pull Requests Link Image]

Then simply click the 'New Pull Request' button and fill out a short description of your changes.
Once you click 'Send Pull Request', a new pull request will be created which will be checked and commented on by a MapDev team member!

