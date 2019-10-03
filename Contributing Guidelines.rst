The process to contributing is as follows:

1. Pick an issue that you want to address/fix and assign it to yourself using the "assignees" section on the right side of the issue's page.
   
   .. image:: guideline_pictures\assign_yourself.png

2. Start a new branch based on the master branch (this is the default behavior for new branches). If you cannot create a branch, this means you have not accepted or been invited to become part of the DVC-Viking-Robotics organization's github account. This is required! If you create a fork to your own github account, testing is entirely on you, and any hardware dependent changes will not be easy to test (if at all -- depending on your access to the supported hardware ie. Raspberry Pi and assorted sensors).
3. If your using Visual Studio Code (highly recommended), you have to set up a debugger configuration. While in the "Debug" section ("1" in screenshot) of th VSCode's sidebar, select ``Add Configuration`` from the drop down menu ("2" in screenshot). This will open up a ``launch.json``. Edit the ``launch.json`` file to look like the following:

   .. image:: guideline_pictures\debugger_setup.png

   .. code-block:: JSON
   
       "configurations": [
           {
               "name": "Python: webapp Module",
               "type": "python",
               "request": "launch",
               "module": "webapp.app",
               "console": "integratedTerminal",
               "args": [
                   "--port", "5555" // this example specifies the default option.
               ]
           }
       ]

   If you are using Visual Studio, the process is a little different. If you're developing in a basic text editor, you can test the webapp repository by using following command in a terminal/command prompt/powershell:

   .. code-block:: shell

       # make sure you are in the webapp repository's root folder
       python -m webapp.app

   To exit, use either the "shutdown server" option from within the webapp's GUI (from the drop-down menu of the power icon in the top right corner) or you could use ``ctrl+c`` in the terminal/command prompt/powershell (this ``keyboardInterupt`` method is only recommended when something has gone terribly wrong).
4. When you have a working solution and you are ready to request a merge of your working branch to master, open a "Pull Request" on the webapp repository's webpage. Make sure that the "Pull Request" at the top of the "create Pull Request page" has an arrow leading from your branch to the master branch. Do not merge the "Pull Request" yourself! You should request a review from one of the github organization's owners (``2bndy5``, ``guidec``, or ``tejashah88``). Again forks will not be tested! Forked contributions' "Pull Request" will be closed. If you have proof (like a screenshot(s)) of your working solution post it in the comments of the "Pull Request".

   .. image:: guideline_pictures\merge_to_master.png

   .. image:: guideline_pictures\assign_reviewers.png
   