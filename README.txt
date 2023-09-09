# Minimal example of ContentAlignment style bug in Avalonia
Styling one of the ContentAlignment properties for a NumericUpDown in App.xml causes the displayed number formatting to not use the format for the current culture. This means that instead of showing '1,0' with the current culture set to fr-FR, the number is shown as '1.0' which matches the culture of the machine.

For computers with a default culture that formats numbers as '1,0' changing the culture to something like 'en-GB' or 'en-US' might also trigger the issue.