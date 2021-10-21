# Controlling VS Code's Suggestions While Typing

If you are ever annoyed with VS Code's suggestions while you are typing, you can control those with settings.  There are settings for almost everything in VS Code.
The official article for these settings can be found here: [https://code.visualstudio.com/docs/editor/intellisense#_settings](https://code.visualstudio.com/docs/editor/intellisense#_settings)

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

Then after saving, those suggestions will go away.
If you ever want those suggestions back you can come back to the settings delete those lines so your settings file is an empty JSON object:

```json
{

}
```
