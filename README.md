# Clone o repositório
```
git clone https://github.com/faccin-eng/dj-commerce
```
# Crie e ative o ambiente virtual python
```
python -m venv .venv
.venv/Scripts/activate
```
# Ative o Django no debugger
Create a debugger launch profile
Switch to Run view in VS Code (using the left-side activity bar or F5). You may see the message "To customize Run and Debug create a launch.json file".
This means that you don't yet have a launch.json file containing debug configurations. VS Code can create that for you if you click on the create a launch.json file link:
Select the link and VS Code will prompt for a debug configuration. Select Django from the dropdown and VS Code will populate a new launch.json file with a Django run configuration.
The launch.json file contains a number of debugging configurations, each of which is a separate JSON object within the configuration array.
Scroll down to and examine the configuration with the name "Python: Django":
```
 "version": "0.2.0",
  "configurations": [
    {
      "name": "Python Debugger: Django",
      "type": "debugpy",
      "request": "launch",
      "program": "${workspaceFolder}\\manage.py",
      "args": ["runserver"],
      "django": true,
      "justMyCode": true
    }
  ]
}
```
Execute com ctrl + F5
