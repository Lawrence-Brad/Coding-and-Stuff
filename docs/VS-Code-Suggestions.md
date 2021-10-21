# Controlling VS Code's Suggestions While Typing

If you are ever annoyed with VS Code's suggestions while you are typing, you can control those with settings.  There are settings for almost everything in VS Code.
The official article for these settings can be found here: [https://code.visualstudio.com/docs/editor/intellisense#_settings](https://code.visualstudio.com/docs/editor/intellisense#_settings)

## Steps to hide automatic suggestions in VS Code

To open your settings go to View > Command Palette

![Command Palette](/Coding-and-Stuff/assets/VSCodeSuggestions/1-CommandPalette.png)

Then at the command prompt that appears type: "Preferences: Open Settings (JSON)" You'll probably have to select the correct one from the drop down list.

![Preferences JSON](/Coding-and-Stuff/assets/VSCodeSuggestions/2-PreferencesJSON.png)

In the JSON settings file, paste in the following so your file looks like:
```json
{
    // Controls if quick suggestions should show up while typing
    "editor.quickSuggestions": {
        "other": false,
        "comments": false,
        "strings": false
    },
    "editor.parameterHints.enabled": false
}
```

When you are done it should look like this:

![settings.json file](/Coding-and-Stuff/assets/VSCodeSuggestions/3-settings.jsonFile.png)


## You can still get the suggestions by using keyboard shortcuts after hiding them
Keyboard shortcuts can be used to get those same suggestions back, even after changing the settings so those shortcuts don't automatically appear.

### Trigger Suggestion
If you still want suggestions, start typing the name you want to use, then use the keyboard shortcut for your OS listed below.

| OS | Shortcut |
|--|--|
| Windows & Linux | <kbd>Ctrl</kbd> + <kbd>Space</kbd> |
| Mac | <kbd>^</kbd> + <kbd>Space</kbd> |

The suggestion will look something like this:

![Trigger Suggestion Example](/Coding-and-Stuff/assets/VSCodeSuggestions/4-TriggerSuggestion.png)

### Trigger Parameter Hints
Paramater hints are great when you might not remember how to use a specific method. To show the hints using the keyboard shortcut, type the method name, then with your cursor inside the parentheses use the following shortcut.

| OS | Shortcut |
|--|--|
| Windows & Linux | <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Space</kbd> |
| Mac | <kbd>^</kbd> + <kbd>⌘</kbd> + <kbd>Space</kbd> |

The parameter hints will look something like this:

![Trigger Parameter Hints Example](/Coding-and-Stuff/assets/VSCodeSuggestions/5-TriggerParameterHints.png)

### VS Code Cheatsheets for your OS
Use the links below to get an official cheat sheet of the keyboard shortcuts for your OS.
| OS | Link |
|--|--|
| Windows | [https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf) |
| Linux | [https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf) |
| Mac | [https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf) |

## Restore automatic suggestions in VS Code by removing the settings
Then after saving, those suggestions will go away.
If you ever want those suggestions back you can come back to the settings delete those lines so your settings file is an empty JSON object:

```json
{

}
```
