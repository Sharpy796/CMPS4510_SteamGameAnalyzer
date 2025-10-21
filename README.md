# CMPS4510_SteamGameAnalyzer
This will be a program to visualize Steam's game metadata by data mining it. More on this to come.

## Running Jupyter Notebook in VSCode
To run your code in Visual Studio Code, you will need a virtual environment ("venv" for short). To create one, follow the below steps. **Keep in mind that this is assuming you have already cloned your repository onto your computer.**

From the Windows search menu (you can find this by pressing the Windows button at the bottom of the screen or on your keyboard), search for **"Anaconda Prompt"**. NOT "Anaconda Navigator"; this is the application to open Jupyter and similar. Anaconda Prompt is the command terminal for Anaconda. If a terminal pops up, you've found the correct application.

In the Anaconda Prompt, type these commands:
```
conda create -n myenv python=3.14.0

conda activate myenv

cd C:\path\to\your\repo\CMPS4510_SteamGameAnalyzer

pip install -r requirements.txt
```

Now, in Visual Studio Code, when you open `project_cluster_cmps451.ipynb`, in the top right corner will be the option to choose which kernel you're using. You'll choose "Python Environments" -> "myenv". Close Visual Studio Code, then reopen it.

If everything went correctly, you should be able to hit "Run All" and everything will run smoothly.

### Adding New Imports
If you need to add a new import and need to install a new library, do so through the Anaconda Prompt. In the prompt, type these commands:
```
conda activate myenv

<your install command here>

cd C:\path\to\your\repo\CMPS4510_SteamGameAnalyzer

pip list --format=freeze > requirements.txt

conda deactivate
```

This will update the `requirements.txt` to include the new library, so that others can easily install the new library. **Make sure to push your code after updating `requirements.txt`.**

### Updating Your Own Imports
If somebody added an import and you need to install the appropriate library, to make sure everybody has the same libraries, do so through the Anaconda Prompt. In the prompt, type these commands:
```
conda activate myenv

cd C:\path\to\your\repo\CMPS4510_SteamGameAnalyzer

pip install -r requirements.txt

conda deactivate
```

Afterward, close and reopen Visual Studio Code, and you should be able to run your code with the appropriate imports.